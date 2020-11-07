---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
ms.openlocfilehash: a8bef03c7ebe7d20e601ece7c25759f590795ef6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704651"
---
# <span data-ttu-id="56281-101">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="56281-101">Get-AzApiManagementGroup</span></span>

## <span data-ttu-id="56281-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="56281-102">SYNOPSIS</span></span>
<span data-ttu-id="56281-103">Pobiera wszystkie lub określone grupy zarządzania API.</span><span class="sxs-lookup"><span data-stu-id="56281-103">Gets all or specific API management groups.</span></span>

## <span data-ttu-id="56281-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="56281-104">SYNTAX</span></span>

### <span data-ttu-id="56281-105">GetAllGroups (domyślny)</span><span class="sxs-lookup"><span data-stu-id="56281-105">GetAllGroups (Default)</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56281-106">GetByGroupId</span><span class="sxs-lookup"><span data-stu-id="56281-106">GetByGroupId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56281-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="56281-107">GetByUserId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56281-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="56281-108">GetByProductId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56281-109">Opis</span><span class="sxs-lookup"><span data-stu-id="56281-109">DESCRIPTION</span></span>
<span data-ttu-id="56281-110">Polecenie cmdlet **Get-AzApiManagementGroup** pobiera wszystkie lub określone grupy zarządzania API.</span><span class="sxs-lookup"><span data-stu-id="56281-110">The **Get-AzApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="56281-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="56281-111">EXAMPLES</span></span>

### <span data-ttu-id="56281-112">Przykład 1: pobieranie wszystkich grup</span><span class="sxs-lookup"><span data-stu-id="56281-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext
```

<span data-ttu-id="56281-113">To polecenie pobiera wszystkie grupy.</span><span class="sxs-lookup"><span data-stu-id="56281-113">This command gets all groups.</span></span>

### <span data-ttu-id="56281-114">Przykład 2: Uzyskiwanie grupy według identyfikatorów</span><span class="sxs-lookup"><span data-stu-id="56281-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="56281-115">To polecenie pobiera identyfikator grupy o nazwie 0123456789.</span><span class="sxs-lookup"><span data-stu-id="56281-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="56281-116">Przykład 3: pobieranie grupy według nazwy</span><span class="sxs-lookup"><span data-stu-id="56281-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="56281-117">To polecenie uzyskuje grupę o nazwie Group0002.</span><span class="sxs-lookup"><span data-stu-id="56281-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="56281-118">Przykład 4: pobieranie wszystkich grup użytkowników</span><span class="sxs-lookup"><span data-stu-id="56281-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="56281-119">To polecenie pobiera wszystkie grupy użytkowników o IDENTYFIKATORze użytkownika o nazwie 0123456789.</span><span class="sxs-lookup"><span data-stu-id="56281-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="56281-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="56281-120">PARAMETERS</span></span>

### <span data-ttu-id="56281-121">-Context</span><span class="sxs-lookup"><span data-stu-id="56281-121">-Context</span></span>
<span data-ttu-id="56281-122">Określa wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="56281-122">Specifies an instance of PsApiManagementContext.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56281-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56281-123">-DefaultProfile</span></span>
<span data-ttu-id="56281-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="56281-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56281-125">-GroupId</span><span class="sxs-lookup"><span data-stu-id="56281-125">-GroupId</span></span>
<span data-ttu-id="56281-126">Określa identyfikator grupy.</span><span class="sxs-lookup"><span data-stu-id="56281-126">Specifies the group ID.</span></span>
<span data-ttu-id="56281-127">Jeśli jest określony, polecenie cmdlet próbuje znaleźć grupę według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="56281-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

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

### <span data-ttu-id="56281-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="56281-128">-Name</span></span>
<span data-ttu-id="56281-129">Określa nazwę grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="56281-129">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="56281-130">-ProductId</span><span class="sxs-lookup"><span data-stu-id="56281-130">-ProductId</span></span>
<span data-ttu-id="56281-131">Identyfikator istniejącego produktu.</span><span class="sxs-lookup"><span data-stu-id="56281-131">Identifier of existing product.</span></span>
<span data-ttu-id="56281-132">Jeśli ta grupa zostanie wybrana, zostaną zwrócone wszystkie grupy, do których przypisano produkt.</span><span class="sxs-lookup"><span data-stu-id="56281-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="56281-133">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="56281-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="56281-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="56281-134">-UserId</span></span>
<span data-ttu-id="56281-135">Określa identyfikator istniejącego produktu.</span><span class="sxs-lookup"><span data-stu-id="56281-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="56281-136">Jeśli zostanie określona, polecenie cmdlet zwróci wszystkie grupy, do których przypisano produkt.</span><span class="sxs-lookup"><span data-stu-id="56281-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

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

### <span data-ttu-id="56281-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56281-137">CommonParameters</span></span>
<span data-ttu-id="56281-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56281-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56281-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56281-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56281-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56281-140">INPUTS</span></span>

### <span data-ttu-id="56281-141">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="56281-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="56281-142">System. String</span><span class="sxs-lookup"><span data-stu-id="56281-142">System.String</span></span>

## <span data-ttu-id="56281-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="56281-143">OUTPUTS</span></span>

### <span data-ttu-id="56281-144">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="56281-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="56281-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="56281-145">NOTES</span></span>

## <span data-ttu-id="56281-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56281-146">RELATED LINKS</span></span>

[<span data-ttu-id="56281-147">Nowe — AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="56281-147">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="56281-148">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="56281-148">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="56281-149">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="56281-149">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


