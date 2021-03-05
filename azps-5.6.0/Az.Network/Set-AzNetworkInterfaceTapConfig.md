---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: a542b69b1f028a7fdfd3e02d02f95735bc4add9f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003345"
---
# <span data-ttu-id="c2f87-101">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="c2f87-101">Set-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="c2f87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2f87-102">SYNOPSIS</span></span>
<span data-ttu-id="c2f87-103">Aktualizuje konfigurację naciśnięcia interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="c2f87-103">Updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="c2f87-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c2f87-104">SYNTAX</span></span>

```
Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig <PSNetworkInterfaceTapConfiguration> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2f87-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c2f87-105">DESCRIPTION</span></span>
<span data-ttu-id="c2f87-106">**Set-AzNetworkInterfaceTapConfig** aktualizuje konfigurację naciśnięcia interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="c2f87-106">The **Set-AzNetworkInterfaceTapConfig** updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="c2f87-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c2f87-107">EXAMPLES</span></span>

### <span data-ttu-id="c2f87-108">Przykład 1. Ustawianie konfiguracji tapconfiguration przy użyciu zaktualizowanej nazwy konfiguracji tapconfig</span><span class="sxs-lookup"><span data-stu-id="c2f87-108">Example 1: Set the TapConfiguration with updated TapConfig name</span></span>
```
PS C:\>$tapConfig = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
PS C:\>$tapConfig.Name = "NewTapName"
PS C:\>Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig $tapConfig
```

## <span data-ttu-id="c2f87-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2f87-109">PARAMETERS</span></span>

### <span data-ttu-id="c2f87-110">— AsJob</span><span class="sxs-lookup"><span data-stu-id="c2f87-110">-AsJob</span></span>
<span data-ttu-id="c2f87-111">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c2f87-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c2f87-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2f87-112">-DefaultProfile</span></span>
<span data-ttu-id="c2f87-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c2f87-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2f87-114">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="c2f87-114">-Force</span></span>
<span data-ttu-id="c2f87-115">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c2f87-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c2f87-116">- NetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="c2f87-116">-NetworkInterfaceTapConfig</span></span>
<span data-ttu-id="c2f87-117">Konfiguracja usługi NetworkInterface Tap</span><span class="sxs-lookup"><span data-stu-id="c2f87-117">The NetworkInterface Tap configuration</span></span>

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

### <span data-ttu-id="c2f87-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c2f87-118">-Confirm</span></span>
<span data-ttu-id="c2f87-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c2f87-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2f87-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2f87-120">-WhatIf</span></span>
<span data-ttu-id="c2f87-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2f87-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2f87-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c2f87-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2f87-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2f87-123">CommonParameters</span></span>
<span data-ttu-id="c2f87-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2f87-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2f87-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2f87-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2f87-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2f87-126">INPUTS</span></span>

### <span data-ttu-id="c2f87-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2f87-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="c2f87-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2f87-128">OUTPUTS</span></span>

### <span data-ttu-id="c2f87-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c2f87-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="c2f87-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c2f87-130">NOTES</span></span>

## <span data-ttu-id="c2f87-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2f87-131">RELATED LINKS</span></span>

[<span data-ttu-id="c2f87-132">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="c2f87-132">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="c2f87-133">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="c2f87-133">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="c2f87-134">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="c2f87-134">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)
