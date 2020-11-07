---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvm
schema: 2.0.0
ms.openlocfilehash: d17d01295d118c3927c127a367747cfde428ccfd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525281"
---
# <span data-ttu-id="f43a4-101">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f43a4-101">Set-AzureRmVM</span></span>

## <span data-ttu-id="f43a4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f43a4-102">SYNOPSIS</span></span>
<span data-ttu-id="f43a4-103">Oznacza maszynę wirtualną jako uogólnioną.</span><span class="sxs-lookup"><span data-stu-id="f43a4-103">Marks a virtual machine as generalized.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f43a4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f43a4-104">SYNTAX</span></span>

### <span data-ttu-id="f43a4-105">GeneralizeResourceGroupNameParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f43a4-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f43a4-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f43a4-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f43a4-107">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f43a4-107">GeneralizeIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f43a4-108">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f43a4-108">RedeployIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Redeploy] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f43a4-109">Opis</span><span class="sxs-lookup"><span data-stu-id="f43a4-109">DESCRIPTION</span></span>
<span data-ttu-id="f43a4-110">Polecenie cmdlet **Set-AzureRmVM** oznacza maszynę wirtualną jako uogólnioną.</span><span class="sxs-lookup"><span data-stu-id="f43a4-110">The **Set-AzureRmVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="f43a4-111">Przed uruchomieniem tego polecenia cmdlet Zaloguj się do maszyny wirtualnej i przygotuj dysk twardy za pomocą narzędzia Sysprep.</span><span class="sxs-lookup"><span data-stu-id="f43a4-111">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="f43a4-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f43a4-112">EXAMPLES</span></span>

### <span data-ttu-id="f43a4-113">Przykład 1. Oznaczanie maszyny wirtualnej jako uogólnionej</span><span class="sxs-lookup"><span data-stu-id="f43a4-113">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="f43a4-114">To polecenie oznacza maszynę wirtualną o nazwie VirtualMachine07 jako uogólnioną.</span><span class="sxs-lookup"><span data-stu-id="f43a4-114">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="f43a4-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f43a4-115">PARAMETERS</span></span>

### <span data-ttu-id="f43a4-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f43a4-116">-AsJob</span></span>
<span data-ttu-id="f43a4-117">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="f43a4-117">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f43a4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f43a4-118">-DefaultProfile</span></span>
<span data-ttu-id="f43a4-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f43a4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f43a4-120">-Uogólniona</span><span class="sxs-lookup"><span data-stu-id="f43a4-120">-Generalized</span></span>
<span data-ttu-id="f43a4-121">Wskazuje, że to polecenie cmdlet oznacza maszynę wirtualną jako uogólnioną.</span><span class="sxs-lookup"><span data-stu-id="f43a4-121">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, GeneralizeIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f43a4-122">-ID</span><span class="sxs-lookup"><span data-stu-id="f43a4-122">-Id</span></span>
<span data-ttu-id="f43a4-123">Określa identyfikator zasobu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f43a4-123">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f43a4-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f43a4-124">-Name</span></span>
<span data-ttu-id="f43a4-125">Określa nazwę maszyny wirtualnej, na której działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f43a4-125">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f43a4-126">-Deploy</span><span class="sxs-lookup"><span data-stu-id="f43a4-126">-Redeploy</span></span>
<span data-ttu-id="f43a4-127">Wskazuje, że to polecenie cmdlet ręcznie ponownie wdraża maszynę wirtualną na innym hoście platformy Azure, aby rozwiązać wszelkie problemy.</span><span class="sxs-lookup"><span data-stu-id="f43a4-127">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>

<span data-ttu-id="f43a4-128">Ponowna instalacja maszyny wirtualnej jest uruchamiana ponownie, co powoduje utratę tymczasowych danych dotyczących dysków.</span><span class="sxs-lookup"><span data-stu-id="f43a4-128">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f43a4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f43a4-129">-ResourceGroupName</span></span>
<span data-ttu-id="f43a4-130">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f43a4-130">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f43a4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f43a4-131">CommonParameters</span></span>
<span data-ttu-id="f43a4-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f43a4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f43a4-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f43a4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f43a4-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f43a4-134">INPUTS</span></span>

### <span data-ttu-id="f43a4-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f43a4-135">None</span></span>
<span data-ttu-id="f43a4-136">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="f43a4-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f43a4-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f43a4-137">OUTPUTS</span></span>

### <span data-ttu-id="f43a4-138">Microsoft. Azure. Commands. COMPUTE. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="f43a4-138">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="f43a4-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f43a4-139">NOTES</span></span>

## <span data-ttu-id="f43a4-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f43a4-140">RELATED LINKS</span></span>

[<span data-ttu-id="f43a4-141">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f43a4-141">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

