# STM32_HAL_TIMER
STM32HAL库的timer定时器使用历程
初始化TIMER定时器HAL_TIM_Base_Start_IT(&htim2);
重构回调函数
void HAL_TIM_PeriodElapsedCallback(TIM_HandleTypeDef *htim)
{
	if(htim->Instance==TIM2)
	{
		HAL_GPIO_TogglePin(GPIOB,GPIO_PIN_8);
	}
}
