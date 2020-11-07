---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVM.md
ms.openlocfilehash: 6fa67a039599ab066b82ad923f5a2f896b0db519
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718548"
---
# <span data-ttu-id="dfef7-101">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="dfef7-101">Set-AzureRmVM</span></span>

## <span data-ttu-id="dfef7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dfef7-102">SYNOPSIS</span></span>
<span data-ttu-id="dfef7-103">Oznacza maszynę wirtualną jako uogólnioną.</span><span class="sxs-lookup"><span data-stu-id="dfef7-103">Marks a virtual machine as generalized.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfef7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dfef7-104">SYNTAX</span></span>

### <span data-ttu-id="dfef7-105">GeneralizeResourceGroupNameParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dfef7-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfef7-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="dfef7-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfef7-107">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="dfef7-107">GeneralizeIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Generalized] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dfef7-108">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="dfef7-108">RedeployIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Redeploy] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dfef7-109">Opis</span><span class="sxs-lookup"><span data-stu-id="dfef7-109">DESCRIPTION</span></span>
<span data-ttu-id="dfef7-110">Polecenie cmdlet **Set-AzureRmVM** oznacza maszynę wirtualną jako uogólnioną.</span><span class="sxs-lookup"><span data-stu-id="dfef7-110">The **Set-AzureRmVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="dfef7-111">Przed uruchomieniem tego polecenia cmdlet Zaloguj się do maszyny wirtualnej i przygotuj dysk twardy za pomocą narzędzia Sysprep.</span><span class="sxs-lookup"><span data-stu-id="dfef7-111">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="dfef7-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dfef7-112">EXAMPLES</span></span>

### <span data-ttu-id="dfef7-113">Przykład 1. Oznaczanie maszyny wirtualnej jako uogólnionej</span><span class="sxs-lookup"><span data-stu-id="dfef7-113">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="dfef7-114">To polecenie oznacza maszynę wirtualną o nazwie VirtualMachine07 jako uogólnioną.</span><span class="sxs-lookup"><span data-stu-id="dfef7-114">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="dfef7-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dfef7-115">PARAMETERS</span></span>

### <span data-ttu-id="dfef7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfef7-116">-DefaultProfile</span></span>
<span data-ttu-id="dfef7-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dfef7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfef7-118">-Uogólniona</span><span class="sxs-lookup"><span data-stu-id="dfef7-118">-Generalized</span></span>
<span data-ttu-id="dfef7-119">Wskazuje, że to polecenie cmdlet oznacza maszynę wirtualną jako uogólnioną.</span><span class="sxs-lookup"><span data-stu-id="dfef7-119">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, GeneralizeIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfef7-120">-ID</span><span class="sxs-lookup"><span data-stu-id="dfef7-120">-Id</span></span>
<span data-ttu-id="dfef7-121">Określa identyfikator zasobu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dfef7-121">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="dfef7-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dfef7-122">-Name</span></span>
<span data-ttu-id="dfef7-123">Określa nazwę maszyny wirtualnej, na której działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfef7-123">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="dfef7-124">-Deploy</span><span class="sxs-lookup"><span data-stu-id="dfef7-124">-Redeploy</span></span>
<span data-ttu-id="dfef7-125">Wskazuje, że to polecenie cmdlet ręcznie ponownie wdraża maszynę wirtualną na innym hoście platformy Azure, aby rozwiązać wszelkie problemy.</span><span class="sxs-lookup"><span data-stu-id="dfef7-125">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>

<span data-ttu-id="dfef7-126">Ponowna instalacja maszyny wirtualnej jest uruchamiana ponownie, co powoduje utratę tymczasowych danych dotyczących dysków.</span><span class="sxs-lookup"><span data-stu-id="dfef7-126">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfef7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfef7-127">-ResourceGroupName</span></span>
<span data-ttu-id="dfef7-128">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dfef7-128">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="dfef7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfef7-129">CommonParameters</span></span>
<span data-ttu-id="dfef7-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfef7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfef7-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfef7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfef7-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dfef7-132">INPUTS</span></span>

## <span data-ttu-id="dfef7-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dfef7-133">OUTPUTS</span></span>

## <span data-ttu-id="dfef7-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dfef7-134">NOTES</span></span>

## <span data-ttu-id="dfef7-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dfef7-135">RELATED LINKS</span></span>

[<span data-ttu-id="dfef7-136">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="dfef7-136">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


