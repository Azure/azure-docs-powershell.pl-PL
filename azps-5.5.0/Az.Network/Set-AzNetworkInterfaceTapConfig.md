---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 31a02e6f27d766d9f74b34c331a69c66e82d8fc5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189451"
---
# <span data-ttu-id="712f1-101">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="712f1-101">Set-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="712f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="712f1-102">SYNOPSIS</span></span>
<span data-ttu-id="712f1-103">Aktualizuje konfigurację naciśnięcia interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="712f1-103">Updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="712f1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="712f1-104">SYNTAX</span></span>

```
Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig <PSNetworkInterfaceTapConfiguration> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="712f1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="712f1-105">DESCRIPTION</span></span>
<span data-ttu-id="712f1-106">**Set-AzNetworkInterfaceTapConfig** aktualizuje konfigurację naciśnięcia dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="712f1-106">The **Set-AzNetworkInterfaceTapConfig** updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="712f1-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="712f1-107">EXAMPLES</span></span>

### <span data-ttu-id="712f1-108">Przykład 1. Ustawianie konfiguracji TapConfiguration ze zaktualizowaną nazwą TapConfig</span><span class="sxs-lookup"><span data-stu-id="712f1-108">Example 1: Set the TapConfiguration with updated TapConfig name</span></span>
```
PS C:\>$tapConfig = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
PS C:\>$tapConfig.Name = "NewTapName"
PS C:\>Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig $tapConfig
```

## <span data-ttu-id="712f1-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="712f1-109">PARAMETERS</span></span>

### <span data-ttu-id="712f1-110">— AsJob</span><span class="sxs-lookup"><span data-stu-id="712f1-110">-AsJob</span></span>
<span data-ttu-id="712f1-111">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="712f1-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="712f1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="712f1-112">-DefaultProfile</span></span>
<span data-ttu-id="712f1-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="712f1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="712f1-114">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="712f1-114">-Force</span></span>
<span data-ttu-id="712f1-115">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="712f1-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="712f1-116">- NetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="712f1-116">-NetworkInterfaceTapConfig</span></span>
<span data-ttu-id="712f1-117">Konfiguracja usługi NetworkInterface Tap</span><span class="sxs-lookup"><span data-stu-id="712f1-117">The NetworkInterface Tap configuration</span></span>

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

### <span data-ttu-id="712f1-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="712f1-118">-Confirm</span></span>
<span data-ttu-id="712f1-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="712f1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="712f1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="712f1-120">-WhatIf</span></span>
<span data-ttu-id="712f1-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="712f1-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="712f1-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="712f1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="712f1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="712f1-123">CommonParameters</span></span>
<span data-ttu-id="712f1-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="712f1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="712f1-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="712f1-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="712f1-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="712f1-126">INPUTS</span></span>

### <span data-ttu-id="712f1-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="712f1-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="712f1-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="712f1-128">OUTPUTS</span></span>

### <span data-ttu-id="712f1-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="712f1-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="712f1-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="712f1-130">NOTES</span></span>

## <span data-ttu-id="712f1-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="712f1-131">RELATED LINKS</span></span>

[<span data-ttu-id="712f1-132">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="712f1-132">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="712f1-133">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="712f1-133">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="712f1-134">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="712f1-134">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)
