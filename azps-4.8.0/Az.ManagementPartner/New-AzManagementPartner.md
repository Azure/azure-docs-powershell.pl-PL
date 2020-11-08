---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/new-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
ms.openlocfilehash: 9e6c56fa48b71e2571b7702e170bdc3e9e41f3aa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064423"
---
# <span data-ttu-id="e5799-101">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="e5799-101">New-AzManagementPartner</span></span>

## <span data-ttu-id="e5799-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e5799-102">SYNOPSIS</span></span>
<span data-ttu-id="e5799-103">Kojarzy identyfikator sieci partnera firmy Microsoft (MPN) z bieżącym użytkownikiem uwierzytelnionym lub usługą.</span><span class="sxs-lookup"><span data-stu-id="e5799-103">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="e5799-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e5799-104">SYNTAX</span></span>

```
New-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5799-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e5799-105">DESCRIPTION</span></span>
<span data-ttu-id="e5799-106">Kojarzy identyfikator sieci partnera firmy Microsoft (MPN) z bieżącym użytkownikiem uwierzytelnionym lub usługą.</span><span class="sxs-lookup"><span data-stu-id="e5799-106">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="e5799-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e5799-107">EXAMPLES</span></span>

### <span data-ttu-id="e5799-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e5799-108">Example 1</span></span>
```powershell
PS C:\> New-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="e5799-109">Dodawanie partnera zarządzania</span><span class="sxs-lookup"><span data-stu-id="e5799-109">Add a management partner</span></span>

## <span data-ttu-id="e5799-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e5799-110">PARAMETERS</span></span>

### <span data-ttu-id="e5799-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5799-111">-DefaultProfile</span></span>
<span data-ttu-id="e5799-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e5799-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5799-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="e5799-113">-PartnerId</span></span>
<span data-ttu-id="e5799-114">Identyfikator partnera zarządzania to numer 6-cyfrowy</span><span class="sxs-lookup"><span data-stu-id="e5799-114">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5799-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e5799-115">-Confirm</span></span>
<span data-ttu-id="e5799-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5799-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5799-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5799-117">-WhatIf</span></span>
<span data-ttu-id="e5799-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5799-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5799-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e5799-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5799-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5799-120">CommonParameters</span></span>
<span data-ttu-id="e5799-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5799-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5799-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5799-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5799-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e5799-123">INPUTS</span></span>

### <span data-ttu-id="e5799-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e5799-124">None</span></span>

## <span data-ttu-id="e5799-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e5799-125">OUTPUTS</span></span>

### <span data-ttu-id="e5799-126">Microsoft. Azure. Commands. ManagementPartner. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="e5799-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="e5799-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e5799-127">NOTES</span></span>

## <span data-ttu-id="e5799-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e5799-128">RELATED LINKS</span></span>

[<span data-ttu-id="e5799-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="e5799-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="e5799-130">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="e5799-130">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="e5799-131">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="e5799-131">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)