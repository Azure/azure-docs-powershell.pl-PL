---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 7b57892316402eab20a14a2761141235a086badb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869536"
---
# <span data-ttu-id="ad072-101">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="ad072-101">Set-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="ad072-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ad072-102">SYNOPSIS</span></span>
<span data-ttu-id="ad072-103">Umożliwia zaktualizowanie konfiguracji naciśnięcia dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="ad072-103">Updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="ad072-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ad072-104">SYNTAX</span></span>

```
Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig <PSNetworkInterfaceTapConfiguration> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad072-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ad072-105">DESCRIPTION</span></span>
<span data-ttu-id="ad072-106">Polecenie **Set-AzNetworkInterfaceTapConfig** aktualizuje konfigurację dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="ad072-106">The **Set-AzNetworkInterfaceTapConfig** updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="ad072-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ad072-107">EXAMPLES</span></span>

### <span data-ttu-id="ad072-108">Przykład 1: Ustawianie TapConfiguration z zaktualizowaną nazwą TapConfig</span><span class="sxs-lookup"><span data-stu-id="ad072-108">Example 1: Set the TapConfiguration with updated TapConfig name</span></span>
```
PS C:\>$tapConfig = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
PS C:\>$tapConfig.Name = "NewTapName"
PS C:\>Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig $tapConfig
```

## <span data-ttu-id="ad072-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ad072-109">PARAMETERS</span></span>

### <span data-ttu-id="ad072-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad072-110">-AsJob</span></span>
<span data-ttu-id="ad072-111">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ad072-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ad072-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad072-112">-DefaultProfile</span></span>
<span data-ttu-id="ad072-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad072-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad072-114">-Force</span><span class="sxs-lookup"><span data-stu-id="ad072-114">-Force</span></span>
<span data-ttu-id="ad072-115">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ad072-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ad072-116">-NetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="ad072-116">-NetworkInterfaceTapConfig</span></span>
<span data-ttu-id="ad072-117">Konfiguracja NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ad072-117">The NetworkInterface Tap configuration</span></span>

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

### <span data-ttu-id="ad072-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ad072-118">-Confirm</span></span>
<span data-ttu-id="ad072-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad072-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad072-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad072-120">-WhatIf</span></span>
<span data-ttu-id="ad072-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad072-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad072-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ad072-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad072-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad072-123">CommonParameters</span></span>
<span data-ttu-id="ad072-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad072-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad072-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad072-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad072-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad072-126">INPUTS</span></span>

### <span data-ttu-id="ad072-127">Microsoft. Azure. Commands. Network. models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad072-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="ad072-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ad072-128">OUTPUTS</span></span>

### <span data-ttu-id="ad072-129">Microsoft. Azure. Commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ad072-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="ad072-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ad072-130">NOTES</span></span>

## <span data-ttu-id="ad072-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad072-131">RELATED LINKS</span></span>

[<span data-ttu-id="ad072-132">Dodaj-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="ad072-132">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="ad072-133">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="ad072-133">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="ad072-134">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="ad072-134">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)
