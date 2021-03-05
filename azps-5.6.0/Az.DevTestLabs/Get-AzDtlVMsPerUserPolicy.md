---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: https://docs.microsoft.com/powershell/module/az.devtestlabs/get-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: 7c2a7ef4c134d811d8c30266305f25d3d53b1289
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004202"
---
# <span data-ttu-id="e1c83-101">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="e1c83-101">Get-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="e1c83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1c83-102">SYNOPSIS</span></span>
<span data-ttu-id="e1c83-103">Pobiera zasady maszyn wirtualnych na użytkownika w laboratorium w laboratorium testów deweloperów.</span><span class="sxs-lookup"><span data-stu-id="e1c83-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="e1c83-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e1c83-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1c83-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e1c83-105">DESCRIPTION</span></span>
<span data-ttu-id="e1c83-106">Polecenie **cmdlet Get-AzDtlVMsPerUserPolicy** pobiera maszyny wirtualne według zasad użytkownika w laboratorium, co pozwala ustawić maksymalną dozwoloną liczbę maszyn wirtualnych na użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e1c83-106">The **Get-AzDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="e1c83-107">Polecenie cmdlet zwraca włączony lub wyłączony stan zasad i maksymalną dozwoloną liczbę maszyn wirtualnych na użytkownika ustawioną w zasadach.</span><span class="sxs-lookup"><span data-stu-id="e1c83-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="e1c83-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e1c83-108">EXAMPLES</span></span>

## <span data-ttu-id="e1c83-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1c83-109">PARAMETERS</span></span>

### <span data-ttu-id="e1c83-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1c83-110">-DefaultProfile</span></span>
<span data-ttu-id="e1c83-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="e1c83-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1c83-112">— LabName</span><span class="sxs-lookup"><span data-stu-id="e1c83-112">-LabName</span></span>
<span data-ttu-id="e1c83-113">Określa nazwę laboratorium, dla którego to polecenie cmdlet pobiera zasady maszyny wirtualnej na użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e1c83-113">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

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

### <span data-ttu-id="e1c83-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1c83-114">-ResourceGroupName</span></span>
<span data-ttu-id="e1c83-115">Określa nazwę grupy zasobów, do której należy laboratorium.</span><span class="sxs-lookup"><span data-stu-id="e1c83-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="e1c83-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1c83-116">CommonParameters</span></span>
<span data-ttu-id="e1c83-117">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1c83-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1c83-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1c83-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1c83-119">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1c83-119">INPUTS</span></span>

### <span data-ttu-id="e1c83-120">System.String</span><span class="sxs-lookup"><span data-stu-id="e1c83-120">System.String</span></span>

## <span data-ttu-id="e1c83-121">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1c83-121">OUTPUTS</span></span>

### <span data-ttu-id="e1c83-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="e1c83-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="e1c83-123">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e1c83-123">NOTES</span></span>

## <span data-ttu-id="e1c83-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1c83-124">RELATED LINKS</span></span>

[<span data-ttu-id="e1c83-125">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="e1c83-125">Set-AzDtlVMsPerUserPolicy</span></span>](./Set-AzDtlVMsPerUserPolicy.md)


