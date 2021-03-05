---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/powershell/module/az.managementpartner/new-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
ms.openlocfilehash: 57d9f5d51cb2646274728f8b2f6d846bd954f2a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994218"
---
# <span data-ttu-id="6f62f-101">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="6f62f-101">New-AzManagementPartner</span></span>

## <span data-ttu-id="6f62f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f62f-102">SYNOPSIS</span></span>
<span data-ttu-id="6f62f-103">Skojarzy identyfikator MPN (Microsoft Partner Network) z bieżącym uwierzytelnionym użytkownikiem lub podmiotem zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="6f62f-103">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="6f62f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6f62f-104">SYNTAX</span></span>

```
New-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6f62f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6f62f-105">DESCRIPTION</span></span>
<span data-ttu-id="6f62f-106">Skojarzy identyfikator MPN (Microsoft Partner Network) z bieżącym uwierzytelnionym użytkownikiem lub podmiotem zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="6f62f-106">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="6f62f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6f62f-107">EXAMPLES</span></span>

### <span data-ttu-id="6f62f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6f62f-108">Example 1</span></span>
```powershell
PS C:\> New-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="6f62f-109">Dodawanie partnera zarządzania</span><span class="sxs-lookup"><span data-stu-id="6f62f-109">Add a management partner</span></span>

## <span data-ttu-id="6f62f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f62f-110">PARAMETERS</span></span>

### <span data-ttu-id="6f62f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f62f-111">-DefaultProfile</span></span>
<span data-ttu-id="6f62f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6f62f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f62f-113">- PartnerId</span><span class="sxs-lookup"><span data-stu-id="6f62f-113">-PartnerId</span></span>
<span data-ttu-id="6f62f-114">Identyfikator partnera zarządzania to 6-cyfrowy numer</span><span class="sxs-lookup"><span data-stu-id="6f62f-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="6f62f-115">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6f62f-115">-Confirm</span></span>
<span data-ttu-id="6f62f-116">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6f62f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f62f-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f62f-117">-WhatIf</span></span>
<span data-ttu-id="6f62f-118">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f62f-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f62f-119">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6f62f-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f62f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f62f-120">CommonParameters</span></span>
<span data-ttu-id="6f62f-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f62f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f62f-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f62f-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f62f-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6f62f-123">INPUTS</span></span>

### <span data-ttu-id="6f62f-124">Brak</span><span class="sxs-lookup"><span data-stu-id="6f62f-124">None</span></span>

## <span data-ttu-id="6f62f-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6f62f-125">OUTPUTS</span></span>

### <span data-ttu-id="6f62f-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="6f62f-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="6f62f-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6f62f-127">NOTES</span></span>

## <span data-ttu-id="6f62f-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6f62f-128">RELATED LINKS</span></span>

[<span data-ttu-id="6f62f-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="6f62f-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="6f62f-130">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="6f62f-130">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="6f62f-131">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="6f62f-131">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)