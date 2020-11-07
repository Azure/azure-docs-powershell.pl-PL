---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 45be0ca132c4a63967b3e7e00fdf3287d8d0b4f8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892853"
---
# <span data-ttu-id="665fa-101">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="665fa-101">Set-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="665fa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="665fa-102">SYNOPSIS</span></span>
<span data-ttu-id="665fa-103">Modyfikuje konfigurację opróżniania połączenia obiektu ustawień HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="665fa-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="665fa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="665fa-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="665fa-105">Opis</span><span class="sxs-lookup"><span data-stu-id="665fa-105">DESCRIPTION</span></span>
<span data-ttu-id="665fa-106">Polecenie cmdlet **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** modyfikuje konfigurację opróżniania połączenia obiektu ustawień http zaplecza.</span><span class="sxs-lookup"><span data-stu-id="665fa-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="665fa-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="665fa-107">EXAMPLES</span></span>

### <span data-ttu-id="665fa-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="665fa-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSetting -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="665fa-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="665fa-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="665fa-110">Drugie polecenie pobiera ustawienia HTTP back-end o nazwie Settings01 dla $AppGw i zapisuje ustawienia w zmiennej $Settings.</span><span class="sxs-lookup"><span data-stu-id="665fa-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="665fa-111">Ostatnie polecenie modyfikuje konfigurację opróżniania połączenia obiektu ustawień https zaplecza przechowywanego w $Settings przez ustawienie wartości FAŁSZ i DrainTimeoutInSec na 3600.</span><span class="sxs-lookup"><span data-stu-id="665fa-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="665fa-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="665fa-112">PARAMETERS</span></span>

### <span data-ttu-id="665fa-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="665fa-113">-BackendHttpSettings</span></span>
<span data-ttu-id="665fa-114">Ustawienia http zaplecza</span><span class="sxs-lookup"><span data-stu-id="665fa-114">The backend http settings</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="665fa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="665fa-115">-DefaultProfile</span></span>
<span data-ttu-id="665fa-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="665fa-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="665fa-117">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="665fa-117">-DrainTimeoutInSec</span></span>
<span data-ttu-id="665fa-118">Liczba sekund opróżniania połączenia jest aktywna.</span><span class="sxs-lookup"><span data-stu-id="665fa-118">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="665fa-119">Dopuszczalne wartości wynoszą od 1 do 3600 sekund.</span><span class="sxs-lookup"><span data-stu-id="665fa-119">Acceptable values are from 1 second to 3600 seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="665fa-120">-Enabled</span><span class="sxs-lookup"><span data-stu-id="665fa-120">-Enabled</span></span>
<span data-ttu-id="665fa-121">Czy opróżnianie połączenia jest włączone, czy nie.</span><span class="sxs-lookup"><span data-stu-id="665fa-121">Whether connection draining is enabled or not.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="665fa-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="665fa-122">CommonParameters</span></span>
<span data-ttu-id="665fa-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="665fa-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="665fa-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="665fa-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="665fa-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="665fa-125">INPUTS</span></span>

### <span data-ttu-id="665fa-126">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="665fa-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="665fa-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="665fa-127">OUTPUTS</span></span>

### <span data-ttu-id="665fa-128">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="665fa-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="665fa-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="665fa-129">NOTES</span></span>

## <span data-ttu-id="665fa-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="665fa-130">RELATED LINKS</span></span>

[<span data-ttu-id="665fa-131">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="665fa-131">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="665fa-132">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="665fa-132">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="665fa-133">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="665fa-133">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="665fa-134">Nowe — AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="665fa-134">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="665fa-135">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="665fa-135">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

