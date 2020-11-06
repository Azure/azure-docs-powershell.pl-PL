---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: A3F653C7-6F9D-4B2B-81F8-0A012D80ECC7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerLabPolicy.md
ms.openlocfilehash: 47e5e6a11e39d8a3f8b1711da8611a9f735fd6b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527593"
---
# <span data-ttu-id="22a3e-101">Get-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="22a3e-101">Get-AzureRmDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="22a3e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="22a3e-102">SYNOPSIS</span></span>
<span data-ttu-id="22a3e-103">Pobiera maszyny wirtualne według zasad laboratorium laboratorium w laboratoriach DevTest.</span><span class="sxs-lookup"><span data-stu-id="22a3e-103">Gets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22a3e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="22a3e-104">SYNTAX</span></span>

```
Get-AzureRmDtlVMsPerLabPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22a3e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="22a3e-105">DESCRIPTION</span></span>
<span data-ttu-id="22a3e-106">Polecenie cmdlet **Get-AzureRmDtlVMsPerLabPolicy** pobiera maszyny wirtualne według zasad laboratorium laboratorium, które umożliwia ustawienie całkowitej liczby maszyn wirtualnych dozwolonych w laboratorium.</span><span class="sxs-lookup"><span data-stu-id="22a3e-106">The **Get-AzureRmDtlVMsPerLabPolicy** cmdlet gets the virtual machines per lab policy of a lab, which allows you set the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="22a3e-107">Polecenie cmdlet zwraca stan włączone lub wyłączone zasady oraz całkowitą liczbę maszyn wirtualnych dozwolonych w laboratorium ustawionym w zasadach.</span><span class="sxs-lookup"><span data-stu-id="22a3e-107">The cmdlet returns the enabled or disabled status of the policy, and the total number of virtual machines allowed in the lab that you have set in the policy.</span></span>

## <span data-ttu-id="22a3e-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="22a3e-108">EXAMPLES</span></span>

## <span data-ttu-id="22a3e-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="22a3e-109">PARAMETERS</span></span>

### <span data-ttu-id="22a3e-110">-LabName</span><span class="sxs-lookup"><span data-stu-id="22a3e-110">-LabName</span></span>
<span data-ttu-id="22a3e-111">Określa nazwę laboratorium, dla którego to polecenie cmdlet pobiera maszyny wirtualne.</span><span class="sxs-lookup"><span data-stu-id="22a3e-111">Specifies the name of the lab for which this cmdlet gets the virtual machines.</span></span>

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

### <span data-ttu-id="22a3e-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22a3e-112">-ResourceGroupName</span></span>
<span data-ttu-id="22a3e-113">Określa nazwę grupy zasobów, do której należy laboratorium.</span><span class="sxs-lookup"><span data-stu-id="22a3e-113">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="22a3e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22a3e-114">-DefaultProfile</span></span>
<span data-ttu-id="22a3e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="22a3e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22a3e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22a3e-116">CommonParameters</span></span>
<span data-ttu-id="22a3e-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22a3e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22a3e-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22a3e-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22a3e-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22a3e-119">INPUTS</span></span>

## <span data-ttu-id="22a3e-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="22a3e-120">OUTPUTS</span></span>

### <span data-ttu-id="22a3e-121">Microsoft. Azure. Commands. DevTestLabs. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="22a3e-121">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="22a3e-122">To polecenie cmdlet zwraca zasadę określającą maksymalną liczbę maszyn wirtualnych, które można utworzyć w laboratorium.</span><span class="sxs-lookup"><span data-stu-id="22a3e-122">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created in the lab.</span></span>

## <span data-ttu-id="22a3e-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="22a3e-123">NOTES</span></span>

## <span data-ttu-id="22a3e-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22a3e-124">RELATED LINKS</span></span>

[<span data-ttu-id="22a3e-125">Set-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="22a3e-125">Set-AzureRmDtlVMsPerLabPolicy</span></span>](./Set-AzureRmDtlVMsPerLabPolicy.md)


