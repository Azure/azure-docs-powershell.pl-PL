---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 25b3f15b6a71b54cbcab1a53f793a32da8b2173a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717004"
---
# <span data-ttu-id="d8392-101">Get-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="d8392-101">Get-AzureRmDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="d8392-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d8392-102">SYNOPSIS</span></span>
<span data-ttu-id="d8392-103">Pobiera dozwolone zasady rozmiarów maszyn wirtualnych w laboratorium w laboratoriach DevTest.</span><span class="sxs-lookup"><span data-stu-id="d8392-103">Gets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8392-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d8392-104">SYNTAX</span></span>

```
Get-AzureRmDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8392-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d8392-105">DESCRIPTION</span></span>
<span data-ttu-id="d8392-106">Polecenie cmdlet **Get-AzureRmDtlAllowedVMSizesPolicy** pobiera dozwolone zasady rozmiarów maszyn wirtualnych, które umożliwiają określenie listy rozmiarów maszyn wirtualnych dozwolonych w laboratorium.</span><span class="sxs-lookup"><span data-stu-id="d8392-106">The **Get-AzureRmDtlAllowedVMSizesPolicy** cmdlet gets the allowed virtual machine sizes policy, which allows you to specify a list of virtual machine sizes allowed in the lab.</span></span>
<span data-ttu-id="d8392-107">Polecenie cmdlet zwraca stan włączone lub wyłączone zasady oraz listę wszystkich dozwolonych rozmiarów maszyn wirtualnych ustawionych w określonych zasadach.</span><span class="sxs-lookup"><span data-stu-id="d8392-107">The cmdlet returns the enabled or disabled status of the policy and a list of all the allowed virtual machine sizes that you have set in the specified policy.</span></span>

## <span data-ttu-id="d8392-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d8392-108">EXAMPLES</span></span>

## <span data-ttu-id="d8392-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d8392-109">PARAMETERS</span></span>

### <span data-ttu-id="d8392-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8392-110">-DefaultProfile</span></span>
<span data-ttu-id="d8392-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d8392-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8392-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="d8392-112">-LabName</span></span>
<span data-ttu-id="d8392-113">Określa nazwę laboratorium, dla którego to polecenie cmdlet pobiera zasady rozmiaru maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="d8392-113">Specifies the name of the lab for which this cmdlet gets virtual machines size policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8392-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8392-114">-ResourceGroupName</span></span>
<span data-ttu-id="d8392-115">Określa nazwę grupy zasobów, do której należy laboratorium.</span><span class="sxs-lookup"><span data-stu-id="d8392-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="d8392-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8392-116">CommonParameters</span></span>
<span data-ttu-id="d8392-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8392-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8392-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8392-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8392-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8392-119">INPUTS</span></span>

### <span data-ttu-id="d8392-120">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d8392-120">None</span></span>
<span data-ttu-id="d8392-121">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="d8392-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d8392-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d8392-122">OUTPUTS</span></span>

### <span data-ttu-id="d8392-123">Microsoft. Azure. Commands. DevTestLabs. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="d8392-123">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="d8392-124">To polecenie cmdlet zwraca zasady określające listę rozmiarów maszyn wirtualnych dozwolonych w laboratorium.</span><span class="sxs-lookup"><span data-stu-id="d8392-124">This cmdlet returns the policy that specifies the list of virtual machine sizes allowed in the lab.</span></span>

## <span data-ttu-id="d8392-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d8392-125">NOTES</span></span>

## <span data-ttu-id="d8392-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8392-126">RELATED LINKS</span></span>

[<span data-ttu-id="d8392-127">Set-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="d8392-127">Set-AzureRmDtlAllowedVMSizesPolicy</span></span>](./Set-AzureRmDtlAllowedVMSizesPolicy.md)

[<span data-ttu-id="d8392-128">Polecenia cmdlet laboratorium testowego środowiska Azure Development</span><span class="sxs-lookup"><span data-stu-id="d8392-128">Azure Development Test Lab Cmdlets</span></span>](./AzureRM.DevTestLabs.md)


