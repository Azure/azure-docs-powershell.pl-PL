---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerUserPolicy.md
ms.openlocfilehash: 53afed94f9733c041df2c49ff1ec97a2fb8277f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542612"
---
# <span data-ttu-id="54fd2-101">Get-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="54fd2-101">Get-AzureRmDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="54fd2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="54fd2-102">SYNOPSIS</span></span>
<span data-ttu-id="54fd2-103">Pobiera maszyny wirtualne według zasad użytkownika laboratorium w laboratoriach DevTest.</span><span class="sxs-lookup"><span data-stu-id="54fd2-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54fd2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="54fd2-104">SYNTAX</span></span>

```
Get-AzureRmDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54fd2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="54fd2-105">DESCRIPTION</span></span>
<span data-ttu-id="54fd2-106">Polecenie cmdlet **Get-AzureRmDtlVMsPerUserPolicy** pobiera maszyny wirtualne według zasad użytkownika laboratorium, które umożliwia ustawienie maksymalnej liczby maszyn wirtualnych dozwolonych dla poszczególnych użytkowników.</span><span class="sxs-lookup"><span data-stu-id="54fd2-106">The **Get-AzureRmDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="54fd2-107">Polecenie cmdlet zwraca stan włączenia lub wyłączenia zasad oraz maksymalną liczbę maszyn wirtualnych dozwolonych dla jednego użytkownika ustawionych w zasadach.</span><span class="sxs-lookup"><span data-stu-id="54fd2-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="54fd2-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="54fd2-108">EXAMPLES</span></span>

## <span data-ttu-id="54fd2-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="54fd2-109">PARAMETERS</span></span>

### <span data-ttu-id="54fd2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54fd2-110">-DefaultProfile</span></span>
<span data-ttu-id="54fd2-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="54fd2-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54fd2-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="54fd2-112">-LabName</span></span>
<span data-ttu-id="54fd2-113">Określa nazwę laboratorium, dla którego to polecenie cmdlet uzyskuje dostęp do zasad maszyny wirtualnej na użytkownika.</span><span class="sxs-lookup"><span data-stu-id="54fd2-113">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

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

### <span data-ttu-id="54fd2-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54fd2-114">-ResourceGroupName</span></span>
<span data-ttu-id="54fd2-115">Określa nazwę grupy zasobów, do której należy laboratorium.</span><span class="sxs-lookup"><span data-stu-id="54fd2-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="54fd2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54fd2-116">CommonParameters</span></span>
<span data-ttu-id="54fd2-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54fd2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54fd2-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54fd2-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54fd2-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="54fd2-119">INPUTS</span></span>

### <span data-ttu-id="54fd2-120">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="54fd2-120">None</span></span>
<span data-ttu-id="54fd2-121">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="54fd2-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="54fd2-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="54fd2-122">OUTPUTS</span></span>

### <span data-ttu-id="54fd2-123">Microsoft. Azure. Commands. DevTestLabs. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="54fd2-123">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="54fd2-124">To polecenie cmdlet zwraca zasadę określającą maksymalną liczbę maszyn wirtualnych, które mogą zostać utworzone przez użytkownika w laboratorium.</span><span class="sxs-lookup"><span data-stu-id="54fd2-124">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created by a user in the lab.</span></span>

## <span data-ttu-id="54fd2-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="54fd2-125">NOTES</span></span>

## <span data-ttu-id="54fd2-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="54fd2-126">RELATED LINKS</span></span>

[<span data-ttu-id="54fd2-127">Set-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="54fd2-127">Set-AzureRmDtlVMsPerUserPolicy</span></span>](./Set-AzureRmDtlVMsPerUserPolicy.md)


