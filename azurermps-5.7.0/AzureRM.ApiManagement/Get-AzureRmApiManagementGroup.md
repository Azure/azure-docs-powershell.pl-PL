---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
ms.openlocfilehash: b77452bff93a9b66f8ffe54fdff623d391749622
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549787"
---
# <span data-ttu-id="aef0c-101">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="aef0c-101">Get-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="aef0c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aef0c-102">SYNOPSIS</span></span>
<span data-ttu-id="aef0c-103">Pobiera wszystkie lub określone grupy zarządzania API.</span><span class="sxs-lookup"><span data-stu-id="aef0c-103">Gets all or specific API management groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aef0c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aef0c-104">SYNTAX</span></span>

### <span data-ttu-id="aef0c-105">GetAllGroups (domyślny)</span><span class="sxs-lookup"><span data-stu-id="aef0c-105">GetAllGroups (Default)</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aef0c-106">GetByGroupId</span><span class="sxs-lookup"><span data-stu-id="aef0c-106">GetByGroupId</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aef0c-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="aef0c-107">GetByUserId</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aef0c-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="aef0c-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aef0c-109">Opis</span><span class="sxs-lookup"><span data-stu-id="aef0c-109">DESCRIPTION</span></span>
<span data-ttu-id="aef0c-110">Polecenie cmdlet **Get-AzureRmApiManagementGroup** pobiera wszystkie lub określone grupy zarządzania API.</span><span class="sxs-lookup"><span data-stu-id="aef0c-110">The **Get-AzureRmApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="aef0c-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aef0c-111">EXAMPLES</span></span>

### <span data-ttu-id="aef0c-112">Przykład 1: pobieranie wszystkich grup</span><span class="sxs-lookup"><span data-stu-id="aef0c-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext
```

<span data-ttu-id="aef0c-113">To polecenie pobiera wszystkie grupy.</span><span class="sxs-lookup"><span data-stu-id="aef0c-113">This command gets all groups.</span></span>

### <span data-ttu-id="aef0c-114">Przykład 2: Uzyskiwanie grupy według identyfikatorów</span><span class="sxs-lookup"><span data-stu-id="aef0c-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="aef0c-115">To polecenie pobiera identyfikator grupy o nazwie 0123456789.</span><span class="sxs-lookup"><span data-stu-id="aef0c-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="aef0c-116">Przykład 3: pobieranie grupy według nazwy</span><span class="sxs-lookup"><span data-stu-id="aef0c-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="aef0c-117">To polecenie uzyskuje grupę o nazwie Group0002.</span><span class="sxs-lookup"><span data-stu-id="aef0c-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="aef0c-118">Przykład 4: pobieranie wszystkich grup użytkowników</span><span class="sxs-lookup"><span data-stu-id="aef0c-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="aef0c-119">To polecenie pobiera wszystkie grupy użytkowników o IDENTYFIKATORze użytkownika o nazwie 0123456789.</span><span class="sxs-lookup"><span data-stu-id="aef0c-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="aef0c-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aef0c-120">PARAMETERS</span></span>

### <span data-ttu-id="aef0c-121">-Context</span><span class="sxs-lookup"><span data-stu-id="aef0c-121">-Context</span></span>
<span data-ttu-id="aef0c-122">Określa wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="aef0c-122">Specifies an instance of PsApiManagementContext.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aef0c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aef0c-123">-DefaultProfile</span></span>
<span data-ttu-id="aef0c-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aef0c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aef0c-125">-GroupId</span><span class="sxs-lookup"><span data-stu-id="aef0c-125">-GroupId</span></span>
<span data-ttu-id="aef0c-126">Określa identyfikator grupy.</span><span class="sxs-lookup"><span data-stu-id="aef0c-126">Specifies the group ID.</span></span>
<span data-ttu-id="aef0c-127">Jeśli jest określony, polecenie cmdlet próbuje znaleźć grupę według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="aef0c-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetByGroupId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aef0c-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aef0c-128">-Name</span></span>
<span data-ttu-id="aef0c-129">Określa nazwę grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="aef0c-129">Specifies the name of the management group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aef0c-130">-ProductId</span><span class="sxs-lookup"><span data-stu-id="aef0c-130">-ProductId</span></span>
<span data-ttu-id="aef0c-131">Identyfikator istniejącego produktu.</span><span class="sxs-lookup"><span data-stu-id="aef0c-131">Identifier of existing product.</span></span>
<span data-ttu-id="aef0c-132">Jeśli ta grupa zostanie wybrana, zostaną zwrócone wszystkie grupy, do których przypisano produkt.</span><span class="sxs-lookup"><span data-stu-id="aef0c-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="aef0c-133">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="aef0c-133">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByProductId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aef0c-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="aef0c-134">-UserId</span></span>
<span data-ttu-id="aef0c-135">Określa identyfikator istniejącego produktu.</span><span class="sxs-lookup"><span data-stu-id="aef0c-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="aef0c-136">Jeśli zostanie określona, polecenie cmdlet zwróci wszystkie grupy, do których przypisano produkt.</span><span class="sxs-lookup"><span data-stu-id="aef0c-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

```yaml
Type: String
Parameter Sets: GetByUserId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aef0c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aef0c-137">CommonParameters</span></span>
<span data-ttu-id="aef0c-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aef0c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aef0c-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aef0c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aef0c-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aef0c-140">INPUTS</span></span>

### <span data-ttu-id="aef0c-141">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="aef0c-141">None</span></span>
<span data-ttu-id="aef0c-142">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="aef0c-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aef0c-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aef0c-143">OUTPUTS</span></span>

### <span data-ttu-id="aef0c-144">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="aef0c-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>
<span data-ttu-id="aef0c-145">Szczegóły grupy skonfigurowanej w usłudze zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="aef0c-145">The details of the Group configured in API Management service.</span></span>

### <span data-ttu-id="aef0c-146">IList<Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementGroup></span><span class="sxs-lookup"><span data-stu-id="aef0c-146">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup></span></span>
<span data-ttu-id="aef0c-147">Lista grup skonfigurowanych w usłudze zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="aef0c-147">The list of Groups configured in API Management service.</span></span>

## <span data-ttu-id="aef0c-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aef0c-148">NOTES</span></span>

## <span data-ttu-id="aef0c-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aef0c-149">RELATED LINKS</span></span>

[<span data-ttu-id="aef0c-150">Nowe — AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="aef0c-150">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="aef0c-151">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="aef0c-151">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)

[<span data-ttu-id="aef0c-152">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="aef0c-152">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


