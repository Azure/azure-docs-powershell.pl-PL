---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: A3F653C7-6F9D-4B2B-81F8-0A012D80ECC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerLabPolicy.md
ms.openlocfilehash: 29d887639dd88f85a24144a4482c40c2b7626c7e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200442"
---
# <span data-ttu-id="d3a0b-101">Get-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="d3a0b-101">Get-AzDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="d3a0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3a0b-102">SYNOPSIS</span></span>
<span data-ttu-id="d3a0b-103">Pobiera maszyny wirtualne na zasady laboratorium w laboratorium DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="d3a0b-103">Gets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="d3a0b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d3a0b-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerLabPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3a0b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d3a0b-105">DESCRIPTION</span></span>
<span data-ttu-id="d3a0b-106">Polecenie **cmdlet Get-AzDtlVMsPerLabPolicy** pobiera maszyny wirtualne na zasady laboratorium, co umożliwia ustawienie całkowitej liczby maszyn wirtualnych dozwolonych w laboratorium.</span><span class="sxs-lookup"><span data-stu-id="d3a0b-106">The **Get-AzDtlVMsPerLabPolicy** cmdlet gets the virtual machines per lab policy of a lab, which allows you set the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="d3a0b-107">Polecenie cmdlet zwraca włączony lub wyłączony stan zasad oraz łączną liczbę maszyn wirtualnych dozwolonych w laboratorium, które zostały ustawione w zasadach.</span><span class="sxs-lookup"><span data-stu-id="d3a0b-107">The cmdlet returns the enabled or disabled status of the policy, and the total number of virtual machines allowed in the lab that you have set in the policy.</span></span>

## <span data-ttu-id="d3a0b-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d3a0b-108">EXAMPLES</span></span>

## <span data-ttu-id="d3a0b-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3a0b-109">PARAMETERS</span></span>

### <span data-ttu-id="d3a0b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3a0b-110">-DefaultProfile</span></span>
<span data-ttu-id="d3a0b-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d3a0b-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3a0b-112">— LabName</span><span class="sxs-lookup"><span data-stu-id="d3a0b-112">-LabName</span></span>
<span data-ttu-id="d3a0b-113">Określa nazwę laboratorium, dla którego to polecenie cmdlet pobiera maszyny wirtualne.</span><span class="sxs-lookup"><span data-stu-id="d3a0b-113">Specifies the name of the lab for which this cmdlet gets the virtual machines.</span></span>

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

### <span data-ttu-id="d3a0b-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3a0b-114">-ResourceGroupName</span></span>
<span data-ttu-id="d3a0b-115">Określa nazwę grupy zasobów, do której należy laboratorium.</span><span class="sxs-lookup"><span data-stu-id="d3a0b-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="d3a0b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3a0b-116">CommonParameters</span></span>
<span data-ttu-id="d3a0b-117">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3a0b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3a0b-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3a0b-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3a0b-119">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3a0b-119">INPUTS</span></span>

### <span data-ttu-id="d3a0b-120">System.String</span><span class="sxs-lookup"><span data-stu-id="d3a0b-120">System.String</span></span>

## <span data-ttu-id="d3a0b-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d3a0b-121">OUTPUTS</span></span>

### <span data-ttu-id="d3a0b-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="d3a0b-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="d3a0b-123">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d3a0b-123">NOTES</span></span>

## <span data-ttu-id="d3a0b-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d3a0b-124">RELATED LINKS</span></span>

[<span data-ttu-id="d3a0b-125">Set-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="d3a0b-125">Set-AzDtlVMsPerLabPolicy</span></span>](./Set-AzDtlVMsPerLabPolicy.md)


