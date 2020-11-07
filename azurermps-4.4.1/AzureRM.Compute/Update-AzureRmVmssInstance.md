---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmssInstance.md
ms.openlocfilehash: 1d7655a78ee2abe00b69d485c35b73cee91ee420
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717178"
---
# <span data-ttu-id="cd355-101">Update-AzureRmVmssInstance</span><span class="sxs-lookup"><span data-stu-id="cd355-101">Update-AzureRmVmssInstance</span></span>

## <span data-ttu-id="cd355-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd355-102">SYNOPSIS</span></span>
<span data-ttu-id="cd355-103">Rozpoczyna ręczne uaktualnienie wystąpienia usługi VMSS.</span><span class="sxs-lookup"><span data-stu-id="cd355-103">Starts a manual upgrade of the VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd355-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd355-104">SYNTAX</span></span>

```
Update-AzureRmVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd355-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cd355-105">DESCRIPTION</span></span>
<span data-ttu-id="cd355-106">Polecenie cmdlet Update-AzureRmVmssInstance rozpoczyna ręczne uaktualnianie określonego wystąpienia zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="cd355-106">The Update-AzureRmVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="cd355-107">Ta funkcja jest używana, gdy w ustawieniach skali VMSS ustawiono wartość ręcznie.</span><span class="sxs-lookup"><span data-stu-id="cd355-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="cd355-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd355-108">EXAMPLES</span></span>

### <span data-ttu-id="cd355-109">Przykład 1. Rozpocznij uaktualnienie wystąpienia programu VMSS</span><span class="sxs-lookup"><span data-stu-id="cd355-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzureRmVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="cd355-110">To polecenie rozpoczyna uaktualnienie VMSS o nazwie VMScaleSet001 o IDENTYFIKATORze wystąpienia 0.</span><span class="sxs-lookup"><span data-stu-id="cd355-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="cd355-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd355-111">PARAMETERS</span></span>

### <span data-ttu-id="cd355-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd355-112">-DefaultProfile</span></span>
<span data-ttu-id="cd355-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd355-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd355-114">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="cd355-114">-InstanceId</span></span>
<span data-ttu-id="cd355-115">Określa, jako tablicę ciągów, identyfikator lub identyfikatory wystąpienia, które ma zostać uaktualnione.</span><span class="sxs-lookup"><span data-stu-id="cd355-115">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd355-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd355-116">-ResourceGroupName</span></span>
<span data-ttu-id="cd355-117">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="cd355-117">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd355-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="cd355-118">-VMScaleSetName</span></span>
<span data-ttu-id="cd355-119">Określa nazwę wystąpienia VMSS, które to polecenie cmdlet jest uaktualniane.</span><span class="sxs-lookup"><span data-stu-id="cd355-119">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd355-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cd355-120">-Confirm</span></span>
<span data-ttu-id="cd355-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd355-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd355-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd355-122">-WhatIf</span></span>
<span data-ttu-id="cd355-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd355-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="cd355-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cd355-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd355-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd355-125">CommonParameters</span></span>
<span data-ttu-id="cd355-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd355-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd355-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd355-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd355-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd355-128">INPUTS</span></span>

## <span data-ttu-id="cd355-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd355-129">OUTPUTS</span></span>

###  
<span data-ttu-id="cd355-130">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="cd355-130">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="cd355-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd355-131">NOTES</span></span>

## <span data-ttu-id="cd355-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd355-132">RELATED LINKS</span></span>

[<span data-ttu-id="cd355-133">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cd355-133">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


