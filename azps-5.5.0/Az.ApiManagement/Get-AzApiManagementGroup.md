---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
ms.openlocfilehash: c7f88f204bbb6d4999e6ddb1f0f3e2942500daf7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239834"
---
# <span data-ttu-id="933b5-101">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="933b5-101">Get-AzApiManagementGroup</span></span>

## <span data-ttu-id="933b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="933b5-102">SYNOPSIS</span></span>
<span data-ttu-id="933b5-103">Pobiera wszystkie lub określone grupy zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="933b5-103">Gets all or specific API management groups.</span></span>

## <span data-ttu-id="933b5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="933b5-104">SYNTAX</span></span>

### <span data-ttu-id="933b5-105">GetAllGroups (Default)</span><span class="sxs-lookup"><span data-stu-id="933b5-105">GetAllGroups (Default)</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="933b5-106">GetByGroupId</span><span class="sxs-lookup"><span data-stu-id="933b5-106">GetByGroupId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="933b5-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="933b5-107">GetByUserId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="933b5-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="933b5-108">GetByProductId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="933b5-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="933b5-109">DESCRIPTION</span></span>
<span data-ttu-id="933b5-110">Polecenie **cmdlet Get-AzApiManagementGroup** pobiera wszystkie lub określone grupy zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="933b5-110">The **Get-AzApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="933b5-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="933b5-111">EXAMPLES</span></span>

### <span data-ttu-id="933b5-112">Przykład 1. Pobierz wszystkie grupy</span><span class="sxs-lookup"><span data-stu-id="933b5-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext
```

<span data-ttu-id="933b5-113">To polecenie pobiera wszystkie grupy.</span><span class="sxs-lookup"><span data-stu-id="933b5-113">This command gets all groups.</span></span>

### <span data-ttu-id="933b5-114">Przykład 2. Uzyskiwanie grupy według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="933b5-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="933b5-115">To polecenie pobiera identyfikator grupy o nazwie 0123456789.</span><span class="sxs-lookup"><span data-stu-id="933b5-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="933b5-116">Przykład 3. Uzyskiwanie grupy według nazwy</span><span class="sxs-lookup"><span data-stu-id="933b5-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="933b5-117">To polecenie pobiera grupę o nazwie Group0002.</span><span class="sxs-lookup"><span data-stu-id="933b5-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="933b5-118">Przykład 4. Pobierz wszystkie grupy użytkowników</span><span class="sxs-lookup"><span data-stu-id="933b5-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="933b5-119">To polecenie pobiera wszystkie grupy użytkowników o identyfikatorze użytkownika 0123456789.</span><span class="sxs-lookup"><span data-stu-id="933b5-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="933b5-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="933b5-120">PARAMETERS</span></span>

### <span data-ttu-id="933b5-121">— kontekst</span><span class="sxs-lookup"><span data-stu-id="933b5-121">-Context</span></span>
<span data-ttu-id="933b5-122">Określa wystąpienie obiektu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="933b5-122">Specifies an instance of PsApiManagementContext.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="933b5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="933b5-123">-DefaultProfile</span></span>
<span data-ttu-id="933b5-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="933b5-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="933b5-125">- GroupId</span><span class="sxs-lookup"><span data-stu-id="933b5-125">-GroupId</span></span>
<span data-ttu-id="933b5-126">Określa identyfikator grupy.</span><span class="sxs-lookup"><span data-stu-id="933b5-126">Specifies the group ID.</span></span>
<span data-ttu-id="933b5-127">Jeśli jest to określone, polecenie cmdlet próbuje znaleźć grupę według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="933b5-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGroupId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="933b5-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="933b5-128">-Name</span></span>
<span data-ttu-id="933b5-129">Określa nazwę grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="933b5-129">Specifies the name of the management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="933b5-130">- ProductId</span><span class="sxs-lookup"><span data-stu-id="933b5-130">-ProductId</span></span>
<span data-ttu-id="933b5-131">Identyfikator istniejącego produktu.</span><span class="sxs-lookup"><span data-stu-id="933b5-131">Identifier of existing product.</span></span>
<span data-ttu-id="933b5-132">Jeśli zostanie określona, zostaną zwrócone wszystkie grupy, do których przypisano produkt.</span><span class="sxs-lookup"><span data-stu-id="933b5-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="933b5-133">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="933b5-133">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="933b5-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="933b5-134">-UserId</span></span>
<span data-ttu-id="933b5-135">Określa identyfikator istniejącego produktu.</span><span class="sxs-lookup"><span data-stu-id="933b5-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="933b5-136">Jeśli to określono, polecenie cmdlet zwróci wszystkie grupy, do których przypisano produkt.</span><span class="sxs-lookup"><span data-stu-id="933b5-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUserId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="933b5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="933b5-137">CommonParameters</span></span>
<span data-ttu-id="933b5-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="933b5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="933b5-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="933b5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="933b5-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="933b5-140">INPUTS</span></span>

### <span data-ttu-id="933b5-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="933b5-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="933b5-142">System.String</span><span class="sxs-lookup"><span data-stu-id="933b5-142">System.String</span></span>

## <span data-ttu-id="933b5-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="933b5-143">OUTPUTS</span></span>

### <span data-ttu-id="933b5-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="933b5-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="933b5-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="933b5-145">NOTES</span></span>

## <span data-ttu-id="933b5-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="933b5-146">RELATED LINKS</span></span>

[<span data-ttu-id="933b5-147">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="933b5-147">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="933b5-148">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="933b5-148">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="933b5-149">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="933b5-149">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


