---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 8e4fbc28d52e8431122b8593b68b909554df6dc9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499218"
---
# <span data-ttu-id="cff0a-101">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="cff0a-101">Get-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="cff0a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cff0a-102">SYNOPSIS</span></span>
<span data-ttu-id="cff0a-103">Pobiera dozwolone zasady rozmiarów maszyn wirtualnych w laboratorium w laboratoriach DevTest.</span><span class="sxs-lookup"><span data-stu-id="cff0a-103">Gets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="cff0a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cff0a-104">SYNTAX</span></span>

```
Get-AzDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cff0a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cff0a-105">DESCRIPTION</span></span>
<span data-ttu-id="cff0a-106">Polecenie cmdlet **Get-AzDtlAllowedVMSizesPolicy** pobiera dozwolone zasady rozmiarów maszyn wirtualnych, które umożliwiają określenie listy rozmiarów maszyn wirtualnych dozwolonych w laboratorium.</span><span class="sxs-lookup"><span data-stu-id="cff0a-106">The **Get-AzDtlAllowedVMSizesPolicy** cmdlet gets the allowed virtual machine sizes policy, which allows you to specify a list of virtual machine sizes allowed in the lab.</span></span>
<span data-ttu-id="cff0a-107">Polecenie cmdlet zwraca stan włączone lub wyłączone zasady oraz listę wszystkich dozwolonych rozmiarów maszyn wirtualnych ustawionych w określonych zasadach.</span><span class="sxs-lookup"><span data-stu-id="cff0a-107">The cmdlet returns the enabled or disabled status of the policy and a list of all the allowed virtual machine sizes that you have set in the specified policy.</span></span>

## <span data-ttu-id="cff0a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cff0a-108">EXAMPLES</span></span>

## <span data-ttu-id="cff0a-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cff0a-109">PARAMETERS</span></span>

### <span data-ttu-id="cff0a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cff0a-110">-DefaultProfile</span></span>
<span data-ttu-id="cff0a-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="cff0a-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cff0a-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="cff0a-112">-LabName</span></span>
<span data-ttu-id="cff0a-113">Określa nazwę laboratorium, dla którego to polecenie cmdlet pobiera zasady rozmiaru maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="cff0a-113">Specifies the name of the lab for which this cmdlet gets virtual machines size policy.</span></span>

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

### <span data-ttu-id="cff0a-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cff0a-114">-ResourceGroupName</span></span>
<span data-ttu-id="cff0a-115">Określa nazwę grupy zasobów, do której należy laboratorium.</span><span class="sxs-lookup"><span data-stu-id="cff0a-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="cff0a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cff0a-116">CommonParameters</span></span>
<span data-ttu-id="cff0a-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cff0a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cff0a-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cff0a-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cff0a-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cff0a-119">INPUTS</span></span>

### <span data-ttu-id="cff0a-120">System. String</span><span class="sxs-lookup"><span data-stu-id="cff0a-120">System.String</span></span>

## <span data-ttu-id="cff0a-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cff0a-121">OUTPUTS</span></span>

### <span data-ttu-id="cff0a-122">Microsoft. Azure. Commands. DevTestLabs. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="cff0a-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="cff0a-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cff0a-123">NOTES</span></span>

## <span data-ttu-id="cff0a-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cff0a-124">RELATED LINKS</span></span>

[<span data-ttu-id="cff0a-125">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="cff0a-125">Set-AzDtlAllowedVMSizesPolicy</span></span>](./Set-AzDtlAllowedVMSizesPolicy.md)


