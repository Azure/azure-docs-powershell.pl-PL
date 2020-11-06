---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmssRollingOSUpgrade.md
ms.openlocfilehash: 7f4e28c00b0238b519ad2b038676a295147b5c0b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549239"
---
# <span data-ttu-id="fcb31-101">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="fcb31-101">Start-AzureRmVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="fcb31-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fcb31-102">SYNOPSIS</span></span>
<span data-ttu-id="fcb31-103">Rozpoczyna uaktualnienie stopniowe, aby przenieść wszystkie wystąpienia zestawu skali maszyny wirtualnej na najnowszą dostępną wersję systemu operacyjnego obrazu platformy.</span><span class="sxs-lookup"><span data-stu-id="fcb31-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcb31-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fcb31-104">SYNTAX</span></span>

```
Start-AzureRmVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcb31-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fcb31-105">DESCRIPTION</span></span>
<span data-ttu-id="fcb31-106">Rozpoczyna uaktualnienie stopniowe, aby przenieść wszystkie wystąpienia zestawu skali maszyny wirtualnej na najnowszą dostępną wersję systemu operacyjnego obrazu platformy.</span><span class="sxs-lookup"><span data-stu-id="fcb31-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="fcb31-107">Wystąpienia, na których jest już uruchomiona najnowsza dostępna wersja systemu operacyjnego, nie mają wpływu.</span><span class="sxs-lookup"><span data-stu-id="fcb31-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="fcb31-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fcb31-108">EXAMPLES</span></span>

### <span data-ttu-id="fcb31-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fcb31-109">Example 1</span></span>
```
PS C:\> Start-AzureRmVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="fcb31-110">To polecenie uruchamia uaktualnianie stopniowe wszystkich wystąpień maszyny wirtualnej "VMSS001" w grupie zasobów "Group001".</span><span class="sxs-lookup"><span data-stu-id="fcb31-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="fcb31-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fcb31-111">PARAMETERS</span></span>

### <span data-ttu-id="fcb31-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcb31-112">-DefaultProfile</span></span>
<span data-ttu-id="fcb31-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fcb31-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcb31-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcb31-114">-ResourceGroupName</span></span>
<span data-ttu-id="fcb31-115">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fcb31-115">The name of the resource group.</span></span>

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

### <span data-ttu-id="fcb31-116">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="fcb31-116">-VMScaleSetName</span></span>
<span data-ttu-id="fcb31-117">Nazwa zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fcb31-117">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="fcb31-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fcb31-118">-Confirm</span></span>
<span data-ttu-id="fcb31-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcb31-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcb31-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcb31-120">-WhatIf</span></span>
<span data-ttu-id="fcb31-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcb31-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcb31-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fcb31-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcb31-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcb31-123">CommonParameters</span></span>
<span data-ttu-id="fcb31-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcb31-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcb31-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcb31-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcb31-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fcb31-126">INPUTS</span></span>

### <span data-ttu-id="fcb31-127">System. String</span><span class="sxs-lookup"><span data-stu-id="fcb31-127">System.String</span></span>

## <span data-ttu-id="fcb31-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fcb31-128">OUTPUTS</span></span>

### <span data-ttu-id="fcb31-129">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="fcb31-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="fcb31-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fcb31-130">NOTES</span></span>

## <span data-ttu-id="fcb31-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fcb31-131">RELATED LINKS</span></span>

