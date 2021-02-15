---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssiptagconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
ms.openlocfilehash: c6af342183b7f1b2aa9bf7695ba8486ec193698a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177642"
---
# <span data-ttu-id="cae36-101">New-AzVmssIpTagConfig</span><span class="sxs-lookup"><span data-stu-id="cae36-101">New-AzVmssIpTagConfig</span></span>

## <span data-ttu-id="cae36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cae36-102">SYNOPSIS</span></span>
<span data-ttu-id="cae36-103">Tworzy obiekt tagu IP dla interfejsu sieciowego maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cae36-103">Creates an IP Tag object for a network interface of a VMSS.</span></span>

## <span data-ttu-id="cae36-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cae36-104">SYNTAX</span></span>

```
New-AzVmssIpTagConfig [-IpTagType] <String> [-Tag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cae36-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="cae36-105">DESCRIPTION</span></span>
<span data-ttu-id="cae36-106">Polecenie **cmdlet New-AzVmssIpTagConfig** tworzy obiekt konfiguracji tagu IP dla interfejsu sieciowego zestawu skal maszyn wirtualnych (VIRTUAL Machine Scale Set).</span><span class="sxs-lookup"><span data-stu-id="cae36-106">The **New-AzVmssIpTagConfig** cmdlet creates an IP Tag configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="cae36-107">Określ konfigurację tego polecenia cmdlet jako parametr *IPTag* New-AzVmssIpConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cae36-107">Specify the configuration from this cmdlet as the *IPTag* parameter of the New-AzVmssIpConfig cmdlet.</span></span>

## <span data-ttu-id="cae36-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cae36-108">EXAMPLES</span></span>

### <span data-ttu-id="cae36-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cae36-109">Example 1</span></span>
```powershell
PS C:\> $iptag = New-AzVmssIpTagConfig -IpTagType 'FirstPartyUsage' -Tag 'Sql'
PS C:\> $ipCfg = New-AzVmssIPConfig -Name 'test' -SubnetId $subnetId -IpTag $ipTag;
```

<span data-ttu-id="cae36-110">To polecenie tworzy obiekt lokalny tagu IP z typem "FirstPartyUsage" i tagiem "Sql", a następnie tworzy konfigurację adresu IP z tym tagiem IP.</span><span class="sxs-lookup"><span data-stu-id="cae36-110">This command creates an IP Tag local object with 'FirstPartyUsage' type and 'Sql' tag, and then creates an IP configuration with this IP tag.</span></span>

## <span data-ttu-id="cae36-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cae36-111">PARAMETERS</span></span>

### <span data-ttu-id="cae36-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cae36-112">-DefaultProfile</span></span>
<span data-ttu-id="cae36-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cae36-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cae36-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="cae36-114">-IpTagType</span></span>
<span data-ttu-id="cae36-115">Określa typ tagu IP.</span><span class="sxs-lookup"><span data-stu-id="cae36-115">Specifies an IP Tag Type.</span></span>

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

### <span data-ttu-id="cae36-116">— Tag</span><span class="sxs-lookup"><span data-stu-id="cae36-116">-Tag</span></span>
<span data-ttu-id="cae36-117">Określa wartość znacznika IP.</span><span class="sxs-lookup"><span data-stu-id="cae36-117">Specifies an IP Tag Value.</span></span>

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

### <span data-ttu-id="cae36-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cae36-118">-Confirm</span></span>
<span data-ttu-id="cae36-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cae36-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cae36-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cae36-120">-WhatIf</span></span>
<span data-ttu-id="cae36-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cae36-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cae36-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cae36-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cae36-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cae36-123">CommonParameters</span></span>
<span data-ttu-id="cae36-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cae36-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cae36-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cae36-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cae36-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cae36-126">INPUTS</span></span>

### <span data-ttu-id="cae36-127">System.String</span><span class="sxs-lookup"><span data-stu-id="cae36-127">System.String</span></span>

## <span data-ttu-id="cae36-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cae36-128">OUTPUTS</span></span>

### <span data-ttu-id="cae36-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span><span class="sxs-lookup"><span data-stu-id="cae36-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span></span>

## <span data-ttu-id="cae36-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cae36-130">NOTES</span></span>

## <span data-ttu-id="cae36-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cae36-131">RELATED LINKS</span></span>
