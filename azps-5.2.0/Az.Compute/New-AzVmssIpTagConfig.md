---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssiptagconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
ms.openlocfilehash: c6af342183b7f1b2aa9bf7695ba8486ec193698a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340078"
---
# <span data-ttu-id="d2d9e-101">New-AzVmssIpTagConfig</span><span class="sxs-lookup"><span data-stu-id="d2d9e-101">New-AzVmssIpTagConfig</span></span>

## <span data-ttu-id="d2d9e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d2d9e-102">SYNOPSIS</span></span>
<span data-ttu-id="d2d9e-103">Tworzy obiekt tagów IP dla interfejsu sieciowego VMSS.</span><span class="sxs-lookup"><span data-stu-id="d2d9e-103">Creates an IP Tag object for a network interface of a VMSS.</span></span>

## <span data-ttu-id="d2d9e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d2d9e-104">SYNTAX</span></span>

```
New-AzVmssIpTagConfig [-IpTagType] <String> [-Tag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2d9e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d2d9e-105">DESCRIPTION</span></span>
<span data-ttu-id="d2d9e-106">Polecenie cmdlet **New-AzVmssIpTagConfig** tworzy obiekt konfiguracji znacznika IP dla interfejsu sieciowego zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="d2d9e-106">The **New-AzVmssIpTagConfig** cmdlet creates an IP Tag configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="d2d9e-107">Określ konfigurację tego polecenia cmdlet jako parametr *IPTag* polecenia cmdlet New-AzVmssIpConfig.</span><span class="sxs-lookup"><span data-stu-id="d2d9e-107">Specify the configuration from this cmdlet as the *IPTag* parameter of the New-AzVmssIpConfig cmdlet.</span></span>

## <span data-ttu-id="d2d9e-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d2d9e-108">EXAMPLES</span></span>

### <span data-ttu-id="d2d9e-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d2d9e-109">Example 1</span></span>
```powershell
PS C:\> $iptag = New-AzVmssIpTagConfig -IpTagType 'FirstPartyUsage' -Tag 'Sql'
PS C:\> $ipCfg = New-AzVmssIPConfig -Name 'test' -SubnetId $subnetId -IpTag $ipTag;
```

<span data-ttu-id="d2d9e-110">To polecenie tworzy obiekt lokalny znacznika IP z typem "FirstPartyUsage" i znacznikiem "SQL", a następnie tworzy konfigurację IP przy użyciu tego znacznika IP.</span><span class="sxs-lookup"><span data-stu-id="d2d9e-110">This command creates an IP Tag local object with 'FirstPartyUsage' type and 'Sql' tag, and then creates an IP configuration with this IP tag.</span></span>

## <span data-ttu-id="d2d9e-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d2d9e-111">PARAMETERS</span></span>

### <span data-ttu-id="d2d9e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2d9e-112">-DefaultProfile</span></span>
<span data-ttu-id="d2d9e-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d2d9e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2d9e-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="d2d9e-114">-IpTagType</span></span>
<span data-ttu-id="d2d9e-115">Określa typ znacznika IP.</span><span class="sxs-lookup"><span data-stu-id="d2d9e-115">Specifies an IP Tag Type.</span></span>

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

### <span data-ttu-id="d2d9e-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="d2d9e-116">-Tag</span></span>
<span data-ttu-id="d2d9e-117">Określa wartość tagu IP.</span><span class="sxs-lookup"><span data-stu-id="d2d9e-117">Specifies an IP Tag Value.</span></span>

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

### <span data-ttu-id="d2d9e-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d2d9e-118">-Confirm</span></span>
<span data-ttu-id="d2d9e-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2d9e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2d9e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2d9e-120">-WhatIf</span></span>
<span data-ttu-id="d2d9e-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2d9e-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2d9e-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d2d9e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2d9e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2d9e-123">CommonParameters</span></span>
<span data-ttu-id="d2d9e-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2d9e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2d9e-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2d9e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2d9e-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2d9e-126">INPUTS</span></span>

### <span data-ttu-id="d2d9e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d2d9e-127">System.String</span></span>

## <span data-ttu-id="d2d9e-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d2d9e-128">OUTPUTS</span></span>

### <span data-ttu-id="d2d9e-129">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSetIpTag</span><span class="sxs-lookup"><span data-stu-id="d2d9e-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span></span>

## <span data-ttu-id="d2d9e-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d2d9e-130">NOTES</span></span>

## <span data-ttu-id="d2d9e-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2d9e-131">RELATED LINKS</span></span>
