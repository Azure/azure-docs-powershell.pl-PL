---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: ae003c3c523c17db9c486edaa68d7e0991b0e6d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549208"
---
# <span data-ttu-id="e732c-101">Get-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="e732c-101">Get-AzureRmDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="e732c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e732c-102">SYNOPSIS</span></span>
<span data-ttu-id="e732c-103">Pobiera dozwolone zasady rozmiarów maszyn wirtualnych w laboratorium w laboratoriach DevTest.</span><span class="sxs-lookup"><span data-stu-id="e732c-103">Gets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e732c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e732c-104">SYNTAX</span></span>

```
Get-AzureRmDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e732c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e732c-105">DESCRIPTION</span></span>
<span data-ttu-id="e732c-106">Polecenie cmdlet **Get-AzureRmDtlAllowedVMSizesPolicy** pobiera dozwolone zasady rozmiarów maszyn wirtualnych, które umożliwiają określenie listy rozmiarów maszyn wirtualnych dozwolonych w laboratorium.</span><span class="sxs-lookup"><span data-stu-id="e732c-106">The **Get-AzureRmDtlAllowedVMSizesPolicy** cmdlet gets the allowed virtual machine sizes policy, which allows you to specify a list of virtual machine sizes allowed in the lab.</span></span>
<span data-ttu-id="e732c-107">Polecenie cmdlet zwraca stan włączone lub wyłączone zasady oraz listę wszystkich dozwolonych rozmiarów maszyn wirtualnych ustawionych w określonych zasadach.</span><span class="sxs-lookup"><span data-stu-id="e732c-107">The cmdlet returns the enabled or disabled status of the policy and a list of all the allowed virtual machine sizes that you have set in the specified policy.</span></span>

## <span data-ttu-id="e732c-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e732c-108">EXAMPLES</span></span>

## <span data-ttu-id="e732c-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e732c-109">PARAMETERS</span></span>

### <span data-ttu-id="e732c-110">-LabName</span><span class="sxs-lookup"><span data-stu-id="e732c-110">-LabName</span></span>
<span data-ttu-id="e732c-111">Określa nazwę laboratorium, dla którego to polecenie cmdlet pobiera zasady rozmiaru maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="e732c-111">Specifies the name of the lab for which this cmdlet gets virtual machines size policy.</span></span>

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

### <span data-ttu-id="e732c-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e732c-112">-ResourceGroupName</span></span>
<span data-ttu-id="e732c-113">Określa nazwę grupy zasobów, do której należy laboratorium.</span><span class="sxs-lookup"><span data-stu-id="e732c-113">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="e732c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e732c-114">-DefaultProfile</span></span>
<span data-ttu-id="e732c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e732c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e732c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e732c-116">CommonParameters</span></span>
<span data-ttu-id="e732c-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e732c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e732c-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e732c-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e732c-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e732c-119">INPUTS</span></span>

## <span data-ttu-id="e732c-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e732c-120">OUTPUTS</span></span>

### <span data-ttu-id="e732c-121">Microsoft. Azure. Commands. DevTestLabs. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="e732c-121">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="e732c-122">To polecenie cmdlet zwraca zasady określające listę rozmiarów maszyn wirtualnych dozwolonych w laboratorium.</span><span class="sxs-lookup"><span data-stu-id="e732c-122">This cmdlet returns the policy that specifies the list of virtual machine sizes allowed in the lab.</span></span>

## <span data-ttu-id="e732c-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e732c-123">NOTES</span></span>

## <span data-ttu-id="e732c-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e732c-124">RELATED LINKS</span></span>

[<span data-ttu-id="e732c-125">Set-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="e732c-125">Set-AzureRmDtlAllowedVMSizesPolicy</span></span>](./Set-AzureRmDtlAllowedVMSizesPolicy.md)

[<span data-ttu-id="e732c-126">Polecenia cmdlet laboratorium testowego środowiska Azure Development</span><span class="sxs-lookup"><span data-stu-id="e732c-126">Azure Development Test Lab Cmdlets</span></span>](./AzureRM.DevTestLabs.md)


