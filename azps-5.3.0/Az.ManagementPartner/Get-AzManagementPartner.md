---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/get-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
ms.openlocfilehash: 1031c9c8828969d16097953aa7440e2c8c0a8c1b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501433"
---
# <span data-ttu-id="132fe-101">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="132fe-101">Get-AzManagementPartner</span></span>

## <span data-ttu-id="132fe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="132fe-102">SYNOPSIS</span></span>
<span data-ttu-id="132fe-103">Pobiera identyfikator sieci partnera firmy Microsoft (MPN) dla bieżącego uwierzytelnionego użytkownika lub usługi.</span><span class="sxs-lookup"><span data-stu-id="132fe-103">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="132fe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="132fe-104">SYNTAX</span></span>

```
Get-AzManagementPartner [[-PartnerId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="132fe-105">Opis</span><span class="sxs-lookup"><span data-stu-id="132fe-105">DESCRIPTION</span></span>
<span data-ttu-id="132fe-106">Pobiera identyfikator sieci partnera firmy Microsoft (MPN) dla bieżącego uwierzytelnionego użytkownika lub usługi.</span><span class="sxs-lookup"><span data-stu-id="132fe-106">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="132fe-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="132fe-107">EXAMPLES</span></span>

### <span data-ttu-id="132fe-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="132fe-108">Example 1</span></span>
```powershell
PS C:\> Get-AzManagementPartner
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="132fe-109">Uzyskiwanie identyfikatora bieżącego partnera zarządzania</span><span class="sxs-lookup"><span data-stu-id="132fe-109">Get the current management partner id</span></span>

### <span data-ttu-id="132fe-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="132fe-110">Example 2</span></span>
```powershell
PS C:\> Get-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="132fe-111">Uzyskaj bieżący identyfikator partnera zarządzania przy użyciu identyfikatora partnera, jeśli nie jest on zgodny, nie powiedzie się</span><span class="sxs-lookup"><span data-stu-id="132fe-111">Get the current management partner id using a partner id, if they don't match, it will fail</span></span>

## <span data-ttu-id="132fe-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="132fe-112">PARAMETERS</span></span>

### <span data-ttu-id="132fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="132fe-113">-DefaultProfile</span></span>
<span data-ttu-id="132fe-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="132fe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="132fe-115">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="132fe-115">-PartnerId</span></span>
<span data-ttu-id="132fe-116">Identyfikator partnera zarządzania to numer 6-cyfrowy</span><span class="sxs-lookup"><span data-stu-id="132fe-116">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="132fe-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="132fe-117">CommonParameters</span></span>
<span data-ttu-id="132fe-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="132fe-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="132fe-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="132fe-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="132fe-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="132fe-120">INPUTS</span></span>

### <span data-ttu-id="132fe-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="132fe-121">None</span></span>

## <span data-ttu-id="132fe-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="132fe-122">OUTPUTS</span></span>

### <span data-ttu-id="132fe-123">Microsoft. Azure. Commands. ManagementPartner. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="132fe-123">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="132fe-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="132fe-124">NOTES</span></span>

## <span data-ttu-id="132fe-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="132fe-125">RELATED LINKS</span></span>

[<span data-ttu-id="132fe-126">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="132fe-126">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="132fe-127">Nowe — AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="132fe-127">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="132fe-128">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="132fe-128">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)