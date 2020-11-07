---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: a147565a61bc75d71083c69766138c3a5a4659db
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868903"
---
# <span data-ttu-id="60050-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="60050-101">Set-AzVM</span></span>

## <span data-ttu-id="60050-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="60050-102">SYNOPSIS</span></span>
<span data-ttu-id="60050-103">Oznacza maszynę wirtualną jako uogólnioną.</span><span class="sxs-lookup"><span data-stu-id="60050-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="60050-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="60050-104">SYNTAX</span></span>

### <span data-ttu-id="60050-105">GeneralizeResourceGroupNameParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="60050-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60050-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="60050-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60050-107">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="60050-107">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [[-Name] <String>] [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="60050-108">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="60050-108">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [[-Name] <String>] [-Redeploy] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="60050-109">Opis</span><span class="sxs-lookup"><span data-stu-id="60050-109">DESCRIPTION</span></span>
<span data-ttu-id="60050-110">Polecenie cmdlet **Set-AzVM** oznacza maszynę wirtualną jako uogólnioną.</span><span class="sxs-lookup"><span data-stu-id="60050-110">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="60050-111">Przed uruchomieniem tego polecenia cmdlet Zaloguj się do maszyny wirtualnej i przygotuj dysk twardy za pomocą narzędzia Sysprep.</span><span class="sxs-lookup"><span data-stu-id="60050-111">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="60050-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="60050-112">EXAMPLES</span></span>

### <span data-ttu-id="60050-113">Przykład 1. Oznaczanie maszyny wirtualnej jako uogólnionej</span><span class="sxs-lookup"><span data-stu-id="60050-113">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="60050-114">To polecenie oznacza maszynę wirtualną o nazwie VirtualMachine07 jako uogólnioną.</span><span class="sxs-lookup"><span data-stu-id="60050-114">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="60050-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="60050-115">PARAMETERS</span></span>

### <span data-ttu-id="60050-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60050-116">-AsJob</span></span>
<span data-ttu-id="60050-117">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="60050-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="60050-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60050-118">-DefaultProfile</span></span>
<span data-ttu-id="60050-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="60050-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60050-120">-Uogólniona</span><span class="sxs-lookup"><span data-stu-id="60050-120">-Generalized</span></span>
<span data-ttu-id="60050-121">Wskazuje, że to polecenie cmdlet oznacza maszynę wirtualną jako uogólnioną.</span><span class="sxs-lookup"><span data-stu-id="60050-121">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, GeneralizeIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60050-122">-ID</span><span class="sxs-lookup"><span data-stu-id="60050-122">-Id</span></span>
<span data-ttu-id="60050-123">Określa identyfikator zasobu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="60050-123">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60050-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="60050-124">-Name</span></span>
<span data-ttu-id="60050-125">Określa nazwę maszyny wirtualnej, na której działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60050-125">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60050-126">-Deploy</span><span class="sxs-lookup"><span data-stu-id="60050-126">-Redeploy</span></span>
<span data-ttu-id="60050-127">Wskazuje, że to polecenie cmdlet ręcznie ponownie wdraża maszynę wirtualną na innym hoście platformy Azure, aby rozwiązać wszelkie problemy.</span><span class="sxs-lookup"><span data-stu-id="60050-127">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="60050-128">Ponowna instalacja maszyny wirtualnej jest uruchamiana ponownie, co powoduje utratę tymczasowych danych dotyczących dysków.</span><span class="sxs-lookup"><span data-stu-id="60050-128">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60050-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60050-129">-ResourceGroupName</span></span>
<span data-ttu-id="60050-130">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="60050-130">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60050-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60050-131">CommonParameters</span></span>
<span data-ttu-id="60050-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60050-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60050-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60050-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60050-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="60050-134">INPUTS</span></span>

### <span data-ttu-id="60050-135">System. String</span><span class="sxs-lookup"><span data-stu-id="60050-135">System.String</span></span>

## <span data-ttu-id="60050-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="60050-136">OUTPUTS</span></span>

### <span data-ttu-id="60050-137">Microsoft. Azure. Commands. COMPUTE. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="60050-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="60050-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="60050-138">NOTES</span></span>

## <span data-ttu-id="60050-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="60050-139">RELATED LINKS</span></span>

[<span data-ttu-id="60050-140">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="60050-140">Get-AzVM</span></span>](./Get-AzVM.md)


