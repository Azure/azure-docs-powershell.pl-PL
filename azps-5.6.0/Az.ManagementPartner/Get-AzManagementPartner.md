---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/powershell/module/az.managementpartner/get-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
ms.openlocfilehash: e09e63ed68ac87156fd03f73c992043b8a0271cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983082"
---
# <span data-ttu-id="46bc3-101">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="46bc3-101">Get-AzManagementPartner</span></span>

## <span data-ttu-id="46bc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46bc3-102">SYNOPSIS</span></span>
<span data-ttu-id="46bc3-103">Pobiera identyfikator MPN (Microsoft Partner Network) bieżącego uwierzytelnionego użytkownika lub podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="46bc3-103">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="46bc3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="46bc3-104">SYNTAX</span></span>

```
Get-AzManagementPartner [[-PartnerId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46bc3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="46bc3-105">DESCRIPTION</span></span>
<span data-ttu-id="46bc3-106">Pobiera identyfikator MPN (Microsoft Partner Network) bieżącego uwierzytelnionego użytkownika lub podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="46bc3-106">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="46bc3-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="46bc3-107">EXAMPLES</span></span>

### <span data-ttu-id="46bc3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="46bc3-108">Example 1</span></span>
```powershell
PS C:\> Get-AzManagementPartner
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="46bc3-109">Uzyskiwanie bieżącego identyfikatora partnera zarządzania</span><span class="sxs-lookup"><span data-stu-id="46bc3-109">Get the current management partner id</span></span>

### <span data-ttu-id="46bc3-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="46bc3-110">Example 2</span></span>
```powershell
PS C:\> Get-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="46bc3-111">Uzyskiwanie bieżącego identyfikatora partnera zarządzania przy użyciu identyfikatora partnera, jeśli jest on nie do siebie dopasowany, nie powiedzie się</span><span class="sxs-lookup"><span data-stu-id="46bc3-111">Get the current management partner id using a partner id, if they don't match, it will fail</span></span>

## <span data-ttu-id="46bc3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46bc3-112">PARAMETERS</span></span>

### <span data-ttu-id="46bc3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46bc3-113">-DefaultProfile</span></span>
<span data-ttu-id="46bc3-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="46bc3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46bc3-115">- PartnerId</span><span class="sxs-lookup"><span data-stu-id="46bc3-115">-PartnerId</span></span>
<span data-ttu-id="46bc3-116">Identyfikator partnera zarządzania to 6-cyfrowy numer</span><span class="sxs-lookup"><span data-stu-id="46bc3-116">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46bc3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46bc3-117">CommonParameters</span></span>
<span data-ttu-id="46bc3-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46bc3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46bc3-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46bc3-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46bc3-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46bc3-120">INPUTS</span></span>

### <span data-ttu-id="46bc3-121">Brak</span><span class="sxs-lookup"><span data-stu-id="46bc3-121">None</span></span>

## <span data-ttu-id="46bc3-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46bc3-122">OUTPUTS</span></span>

### <span data-ttu-id="46bc3-123">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="46bc3-123">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="46bc3-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="46bc3-124">NOTES</span></span>

## <span data-ttu-id="46bc3-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46bc3-125">RELATED LINKS</span></span>

[<span data-ttu-id="46bc3-126">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="46bc3-126">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="46bc3-127">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="46bc3-127">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="46bc3-128">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="46bc3-128">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)