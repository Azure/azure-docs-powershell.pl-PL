---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
ms.openlocfilehash: c7f88f204bbb6d4999e6ddb1f0f3e2942500daf7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365416"
---
# <span data-ttu-id="b5ff4-101">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b5ff4-101">Get-AzApiManagementGroup</span></span>

## <span data-ttu-id="b5ff4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b5ff4-102">SYNOPSIS</span></span>
<span data-ttu-id="b5ff4-103">Pobiera wszystkie lub określone grupy zarządzania API.</span><span class="sxs-lookup"><span data-stu-id="b5ff4-103">Gets all or specific API management groups.</span></span>

## <span data-ttu-id="b5ff4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b5ff4-104">SYNTAX</span></span>

### <span data-ttu-id="b5ff4-105">GetAllGroups (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b5ff4-105">GetAllGroups (Default)</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5ff4-106">GetByGroupId</span><span class="sxs-lookup"><span data-stu-id="b5ff4-106">GetByGroupId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5ff4-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="b5ff4-107">GetByUserId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5ff4-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="b5ff4-108">GetByProductId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5ff4-109">Opis</span><span class="sxs-lookup"><span data-stu-id="b5ff4-109">DESCRIPTION</span></span>
<span data-ttu-id="b5ff4-110">Polecenie cmdlet **Get-AzApiManagementGroup** pobiera wszystkie lub określone grupy zarządzania API.</span><span class="sxs-lookup"><span data-stu-id="b5ff4-110">The **Get-AzApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="b5ff4-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b5ff4-111">EXAMPLES</span></span>

### <span data-ttu-id="b5ff4-112">Przykład 1: pobieranie wszystkich grup</span><span class="sxs-lookup"><span data-stu-id="b5ff4-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext
```

<span data-ttu-id="b5ff4-113">To polecenie pobiera wszystkie grupy.</span><span class="sxs-lookup"><span data-stu-id="b5ff4-113">This command gets all groups.</span></span>

### <span data-ttu-id="b5ff4-114">Przykład 2: Uzyskiwanie grupy według identyfikatorów</span><span class="sxs-lookup"><span data-stu-id="b5ff4-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="b5ff4-115">To polecenie pobiera identyfikator grupy o nazwie 0123456789.</span><span class="sxs-lookup"><span data-stu-id="b5ff4-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="b5ff4-116">Przykład 3: pobieranie grupy według nazwy</span><span class="sxs-lookup"><span data-stu-id="b5ff4-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="b5ff4-117">To polecenie uzyskuje grupę o nazwie Group0002.</span><span class="sxs-lookup"><span data-stu-id="b5ff4-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="b5ff4-118">Przykład 4: pobieranie wszystkich grup użytkowników</span><span class="sxs-lookup"><span data-stu-id="b5ff4-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="b5ff4-119">To polecenie pobiera wszystkie grupy użytkowników o IDENTYFIKATORze użytkownika o nazwie 0123456789.</span><span class="sxs-lookup"><span data-stu-id="b5ff4-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="b5ff4-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b5ff4-120">PARAMETERS</span></span>

### <span data-ttu-id="b5ff4-121">-Context</span><span class="sxs-lookup"><span data-stu-id="b5ff4-121">-Context</span></span>
<span data-ttu-id="b5ff4-122">Określa wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b5ff4-122">Specifies an instance of PsApiManagementContext.</span></span>

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

### <span data-ttu-id="b5ff4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5ff4-123">-DefaultProfile</span></span>
<span data-ttu-id="b5ff4-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b5ff4-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5ff4-125">-GroupId</span><span class="sxs-lookup"><span data-stu-id="b5ff4-125">-GroupId</span></span>
<span data-ttu-id="b5ff4-126">Określa identyfikator grupy.</span><span class="sxs-lookup"><span data-stu-id="b5ff4-126">Specifies the group ID.</span></span>
<span data-ttu-id="b5ff4-127">Jeśli jest określony, polecenie cmdlet próbuje znaleźć grupę według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="b5ff4-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

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

### <span data-ttu-id="b5ff4-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b5ff4-128">-Name</span></span>
<span data-ttu-id="b5ff4-129">Określa nazwę grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="b5ff4-129">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="b5ff4-130">-ProductId</span><span class="sxs-lookup"><span data-stu-id="b5ff4-130">-ProductId</span></span>
<span data-ttu-id="b5ff4-131">Identyfikator istniejącego produktu.</span><span class="sxs-lookup"><span data-stu-id="b5ff4-131">Identifier of existing product.</span></span>
<span data-ttu-id="b5ff4-132">Jeśli ta grupa zostanie wybrana, zostaną zwrócone wszystkie grupy, do których przypisano produkt.</span><span class="sxs-lookup"><span data-stu-id="b5ff4-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="b5ff4-133">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b5ff4-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="b5ff4-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="b5ff4-134">-UserId</span></span>
<span data-ttu-id="b5ff4-135">Określa identyfikator istniejącego produktu.</span><span class="sxs-lookup"><span data-stu-id="b5ff4-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="b5ff4-136">Jeśli zostanie określona, polecenie cmdlet zwróci wszystkie grupy, do których przypisano produkt.</span><span class="sxs-lookup"><span data-stu-id="b5ff4-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

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

### <span data-ttu-id="b5ff4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5ff4-137">CommonParameters</span></span>
<span data-ttu-id="b5ff4-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5ff4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5ff4-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5ff4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5ff4-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5ff4-140">INPUTS</span></span>

### <span data-ttu-id="b5ff4-141">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b5ff4-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b5ff4-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b5ff4-142">System.String</span></span>

## <span data-ttu-id="b5ff4-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b5ff4-143">OUTPUTS</span></span>

### <span data-ttu-id="b5ff4-144">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b5ff4-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="b5ff4-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b5ff4-145">NOTES</span></span>

## <span data-ttu-id="b5ff4-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5ff4-146">RELATED LINKS</span></span>

[<span data-ttu-id="b5ff4-147">Nowe — AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b5ff4-147">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="b5ff4-148">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b5ff4-148">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="b5ff4-149">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b5ff4-149">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


