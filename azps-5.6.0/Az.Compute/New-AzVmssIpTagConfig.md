---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmssiptagconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
ms.openlocfilehash: 241b8938be77d9074000a116f82d8b2bcdffc5b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007073"
---
# <span data-ttu-id="71750-101">New-AzVmssIpTagConfig</span><span class="sxs-lookup"><span data-stu-id="71750-101">New-AzVmssIpTagConfig</span></span>

## <span data-ttu-id="71750-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71750-102">SYNOPSIS</span></span>
<span data-ttu-id="71750-103">Tworzy obiekt tagu IP dla interfejsu sieciowego maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="71750-103">Creates an IP Tag object for a network interface of a VMSS.</span></span>

## <span data-ttu-id="71750-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="71750-104">SYNTAX</span></span>

```
New-AzVmssIpTagConfig [-IpTagType] <String> [-Tag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71750-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="71750-105">DESCRIPTION</span></span>
<span data-ttu-id="71750-106">Polecenie **cmdlet New-AzVmssIpTagConfig** tworzy obiekt konfiguracji tagu IP dla interfejsu sieciowego zestawu skal maszyn wirtualnych (VIRTUAL Machine Scale Set).</span><span class="sxs-lookup"><span data-stu-id="71750-106">The **New-AzVmssIpTagConfig** cmdlet creates an IP Tag configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="71750-107">Określ konfigurację tego polecenia cmdlet jako parametr *IPTag* New-AzVmssIpConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71750-107">Specify the configuration from this cmdlet as the *IPTag* parameter of the New-AzVmssIpConfig cmdlet.</span></span>

## <span data-ttu-id="71750-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="71750-108">EXAMPLES</span></span>

### <span data-ttu-id="71750-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="71750-109">Example 1</span></span>
```powershell
PS C:\> $iptag = New-AzVmssIpTagConfig -IpTagType 'FirstPartyUsage' -Tag 'Sql'
PS C:\> $ipCfg = New-AzVmssIPConfig -Name 'test' -SubnetId $subnetId -IpTag $ipTag;
```

<span data-ttu-id="71750-110">To polecenie tworzy obiekt lokalny tagu IP z typem "FirstPartyUsage" i tagiem "Sql", a następnie tworzy konfigurację adresu IP z tym tagiem IP.</span><span class="sxs-lookup"><span data-stu-id="71750-110">This command creates an IP Tag local object with 'FirstPartyUsage' type and 'Sql' tag, and then creates an IP configuration with this IP tag.</span></span>

## <span data-ttu-id="71750-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71750-111">PARAMETERS</span></span>

### <span data-ttu-id="71750-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71750-112">-DefaultProfile</span></span>
<span data-ttu-id="71750-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="71750-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71750-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="71750-114">-IpTagType</span></span>
<span data-ttu-id="71750-115">Określa typ tagu IP.</span><span class="sxs-lookup"><span data-stu-id="71750-115">Specifies an IP Tag Type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71750-116">— Tag</span><span class="sxs-lookup"><span data-stu-id="71750-116">-Tag</span></span>
<span data-ttu-id="71750-117">Określa wartość znacznika IP.</span><span class="sxs-lookup"><span data-stu-id="71750-117">Specifies an IP Tag Value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71750-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="71750-118">-Confirm</span></span>
<span data-ttu-id="71750-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="71750-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71750-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71750-120">-WhatIf</span></span>
<span data-ttu-id="71750-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71750-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71750-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="71750-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71750-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71750-123">CommonParameters</span></span>
<span data-ttu-id="71750-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71750-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71750-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71750-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71750-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71750-126">INPUTS</span></span>

### <span data-ttu-id="71750-127">System.String</span><span class="sxs-lookup"><span data-stu-id="71750-127">System.String</span></span>

## <span data-ttu-id="71750-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71750-128">OUTPUTS</span></span>

### <span data-ttu-id="71750-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span><span class="sxs-lookup"><span data-stu-id="71750-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span></span>

## <span data-ttu-id="71750-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="71750-130">NOTES</span></span>

## <span data-ttu-id="71750-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71750-131">RELATED LINKS</span></span>
