---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: f2d8604de126dcdfa830bdd6650cf66a6db391b5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051355"
---
# <span data-ttu-id="9cfa4-101">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="9cfa4-101">Get-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="9cfa4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9cfa4-102">SYNOPSIS</span></span>
<span data-ttu-id="9cfa4-103">Pobiera maszyny wirtualne według zasad użytkownika laboratorium w laboratoriach DevTest.</span><span class="sxs-lookup"><span data-stu-id="9cfa4-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="9cfa4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9cfa4-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9cfa4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9cfa4-105">DESCRIPTION</span></span>
<span data-ttu-id="9cfa4-106">Polecenie cmdlet **Get-AzDtlVMsPerUserPolicy** pobiera maszyny wirtualne według zasad użytkownika laboratorium, które umożliwia ustawienie maksymalnej liczby maszyn wirtualnych dozwolonych dla poszczególnych użytkowników.</span><span class="sxs-lookup"><span data-stu-id="9cfa4-106">The **Get-AzDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="9cfa4-107">Polecenie cmdlet zwraca stan włączenia lub wyłączenia zasad oraz maksymalną liczbę maszyn wirtualnych dozwolonych dla jednego użytkownika ustawionych w zasadach.</span><span class="sxs-lookup"><span data-stu-id="9cfa4-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="9cfa4-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9cfa4-108">EXAMPLES</span></span>

## <span data-ttu-id="9cfa4-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9cfa4-109">PARAMETERS</span></span>

### <span data-ttu-id="9cfa4-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cfa4-110">-DefaultProfile</span></span>
<span data-ttu-id="9cfa4-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9cfa4-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9cfa4-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="9cfa4-112">-LabName</span></span>
<span data-ttu-id="9cfa4-113">Określa nazwę laboratorium, dla którego to polecenie cmdlet uzyskuje dostęp do zasad maszyny wirtualnej na użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9cfa4-113">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

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

### <span data-ttu-id="9cfa4-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cfa4-114">-ResourceGroupName</span></span>
<span data-ttu-id="9cfa4-115">Określa nazwę grupy zasobów, do której należy laboratorium.</span><span class="sxs-lookup"><span data-stu-id="9cfa4-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="9cfa4-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cfa4-116">CommonParameters</span></span>
<span data-ttu-id="9cfa4-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cfa4-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cfa4-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cfa4-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cfa4-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9cfa4-119">INPUTS</span></span>

### <span data-ttu-id="9cfa4-120">System. String</span><span class="sxs-lookup"><span data-stu-id="9cfa4-120">System.String</span></span>

## <span data-ttu-id="9cfa4-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9cfa4-121">OUTPUTS</span></span>

### <span data-ttu-id="9cfa4-122">Microsoft. Azure. Commands. DevTestLabs. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="9cfa4-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="9cfa4-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9cfa4-123">NOTES</span></span>

## <span data-ttu-id="9cfa4-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9cfa4-124">RELATED LINKS</span></span>

[<span data-ttu-id="9cfa4-125">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="9cfa4-125">Set-AzDtlVMsPerUserPolicy</span></span>](./Set-AzDtlVMsPerUserPolicy.md)


