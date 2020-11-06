---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssiptagconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssIpTagConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssIpTagConfig.md
ms.openlocfilehash: a77680921eeef0a678cbd83d04bef9a51cf35cb3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524546"
---
# <span data-ttu-id="87c29-101">New-AzureRmVmssIpTagConfig</span><span class="sxs-lookup"><span data-stu-id="87c29-101">New-AzureRmVmssIpTagConfig</span></span>

## <span data-ttu-id="87c29-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="87c29-102">SYNOPSIS</span></span>
<span data-ttu-id="87c29-103">Tworzy obiekt tagów IP dla interfejsu sieciowego VMSS.</span><span class="sxs-lookup"><span data-stu-id="87c29-103">Creates an IP Tag object for a network interface of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87c29-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="87c29-104">SYNTAX</span></span>

```
New-AzureRmVmssIpTagConfig [-IpTagType] <String> [-Tag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87c29-105">Opis</span><span class="sxs-lookup"><span data-stu-id="87c29-105">DESCRIPTION</span></span>
<span data-ttu-id="87c29-106">Polecenie cmdlet **New-AzureRmVmssIpTagConfig** tworzy obiekt konfiguracji znacznika IP dla interfejsu sieciowego zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="87c29-106">The **New-AzureRmVmssIpTagConfig** cmdlet creates an IP Tag configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="87c29-107">Określ konfigurację tego polecenia cmdlet jako parametr *IPTag* polecenia cmdlet New-AzureRmVmssIpConfig.</span><span class="sxs-lookup"><span data-stu-id="87c29-107">Specify the configuration from this cmdlet as the *IPTag* parameter of the New-AzureRmVmssIpConfig cmdlet.</span></span>

## <span data-ttu-id="87c29-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="87c29-108">EXAMPLES</span></span>

### <span data-ttu-id="87c29-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="87c29-109">Example 1</span></span>
```powershell
PS C:\> $iptag = New-AzureRmVmssIpTagConfig -IpTagType 'FirstPartyUsage' -Tag 'Sql'
PS C:\> $ipCfg = New-AzureRmVmssIPConfig -Name 'test' -SubnetId $subnetId -IpTag $ipTag;
```

<span data-ttu-id="87c29-110">To polecenie tworzy obiekt lokalny znacznika IP z typem "FirstPartyUsage" i znacznikiem "SQL", a następnie tworzy konfigurację IP przy użyciu tego znacznika IP.</span><span class="sxs-lookup"><span data-stu-id="87c29-110">This command creates an IP Tag local object with 'FirstPartyUsage' type and 'Sql' tag, and then creates an IP configuration with this IP tag.</span></span>

## <span data-ttu-id="87c29-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="87c29-111">PARAMETERS</span></span>

### <span data-ttu-id="87c29-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87c29-112">-DefaultProfile</span></span>
<span data-ttu-id="87c29-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="87c29-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87c29-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="87c29-114">-IpTagType</span></span>
<span data-ttu-id="87c29-115">Określa typ znacznika IP.</span><span class="sxs-lookup"><span data-stu-id="87c29-115">Specifies an IP Tag Type.</span></span>

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

### <span data-ttu-id="87c29-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="87c29-116">-Tag</span></span>
<span data-ttu-id="87c29-117">Określa wartość tagu IP.</span><span class="sxs-lookup"><span data-stu-id="87c29-117">Specifies an IP Tag Value.</span></span>

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

### <span data-ttu-id="87c29-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="87c29-118">-Confirm</span></span>
<span data-ttu-id="87c29-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87c29-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87c29-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87c29-120">-WhatIf</span></span>
<span data-ttu-id="87c29-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87c29-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87c29-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="87c29-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87c29-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87c29-123">CommonParameters</span></span>
<span data-ttu-id="87c29-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87c29-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87c29-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87c29-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87c29-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87c29-126">INPUTS</span></span>

### <span data-ttu-id="87c29-127">System. String</span><span class="sxs-lookup"><span data-stu-id="87c29-127">System.String</span></span>

## <span data-ttu-id="87c29-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="87c29-128">OUTPUTS</span></span>

### <span data-ttu-id="87c29-129">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSetIpTag</span><span class="sxs-lookup"><span data-stu-id="87c29-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span></span>

## <span data-ttu-id="87c29-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="87c29-130">NOTES</span></span>

## <span data-ttu-id="87c29-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87c29-131">RELATED LINKS</span></span>
