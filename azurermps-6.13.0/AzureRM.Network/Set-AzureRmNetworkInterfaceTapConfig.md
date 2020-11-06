---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterfaceTapConfig.md
ms.openlocfilehash: b2034f27cb6c5332b190e3412963dde99f4c9ba0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524353"
---
# <span data-ttu-id="29a96-101">Set-AzureRmNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="29a96-101">Set-AzureRmNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="29a96-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="29a96-102">SYNOPSIS</span></span>
<span data-ttu-id="29a96-103">Ustawia stan celu dla konfiguracji TAP</span><span class="sxs-lookup"><span data-stu-id="29a96-103">Sets the goal state of a Tap Configuration</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29a96-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="29a96-104">SYNTAX</span></span>

```
Set-AzureRmNetworkInterfaceTapConfig -NetworkInterfaceTapConfig <PSNetworkInterfaceTapConfiguration> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29a96-105">Opis</span><span class="sxs-lookup"><span data-stu-id="29a96-105">DESCRIPTION</span></span>
<span data-ttu-id="29a96-106">**Zestaw-AzureRmNetworkInterfaceTapConfig** ustawia stan celu dla interfejsu sieciowego platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="29a96-106">The **Set-AzureRmNetworkInterfaceTapConfig** sets the goal state for an Azure network interface.</span></span>

## <span data-ttu-id="29a96-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="29a96-107">EXAMPLES</span></span>

### <span data-ttu-id="29a96-108">Przykład 1: Ustawianie TapConfiguration z zaktualizowaną nazwą TapConfig</span><span class="sxs-lookup"><span data-stu-id="29a96-108">Example 1: Set the TapConfiguration with updated TapConfig name</span></span>
```
PS C:\>$tapConfig = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
PS C:\>$tapConfig.Name = "NewTapName"
PS C:\>Set-AzureRmNetworkInterfaceTapConfig -NetworkInterfaceTapConfig $tapConfig
```

## <span data-ttu-id="29a96-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="29a96-109">PARAMETERS</span></span>

### <span data-ttu-id="29a96-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29a96-110">-AsJob</span></span>
<span data-ttu-id="29a96-111">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="29a96-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29a96-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29a96-112">-DefaultProfile</span></span>
<span data-ttu-id="29a96-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="29a96-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29a96-114">-Force</span><span class="sxs-lookup"><span data-stu-id="29a96-114">-Force</span></span>
<span data-ttu-id="29a96-115">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="29a96-115">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29a96-116">-NetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="29a96-116">-NetworkInterfaceTapConfig</span></span>
<span data-ttu-id="29a96-117">NetworkInterface naciśnij configurtion</span><span class="sxs-lookup"><span data-stu-id="29a96-117">The NetworkInterface Tap configurtion</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29a96-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="29a96-118">-Confirm</span></span>
<span data-ttu-id="29a96-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29a96-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29a96-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29a96-120">-WhatIf</span></span>
<span data-ttu-id="29a96-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29a96-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29a96-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="29a96-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29a96-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29a96-123">CommonParameters</span></span>
<span data-ttu-id="29a96-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29a96-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29a96-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29a96-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29a96-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29a96-126">INPUTS</span></span>

### <span data-ttu-id="29a96-127">Microsoft. Azure. Commands. Network. models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="29a96-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="29a96-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="29a96-128">OUTPUTS</span></span>

### <span data-ttu-id="29a96-129">Microsoft. Azure. Commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="29a96-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="29a96-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="29a96-130">NOTES</span></span>

## <span data-ttu-id="29a96-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29a96-131">RELATED LINKS</span></span>
