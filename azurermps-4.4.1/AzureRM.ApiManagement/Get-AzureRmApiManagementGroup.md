---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
ms.openlocfilehash: 0c28742eb3c774adb8c7b6a8d920e91377bea35f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548435"
---
# <span data-ttu-id="09ffb-101">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="09ffb-101">Get-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="09ffb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="09ffb-102">SYNOPSIS</span></span>
<span data-ttu-id="09ffb-103">Pobiera wszystkie lub określone grupy zarządzania API.</span><span class="sxs-lookup"><span data-stu-id="09ffb-103">Gets all or specific API management groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09ffb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="09ffb-104">SYNTAX</span></span>

### <span data-ttu-id="09ffb-105">Pobieranie wszystkich grup (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="09ffb-105">Get all groups (Default)</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09ffb-106">Identyfikator grupy</span><span class="sxs-lookup"><span data-stu-id="09ffb-106">Get by group ID</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09ffb-107">Znajdowanie grup według użytkowników</span><span class="sxs-lookup"><span data-stu-id="09ffb-107">Find groups by user</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09ffb-108">Znajdowanie grup według produktów</span><span class="sxs-lookup"><span data-stu-id="09ffb-108">Find groups by product</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09ffb-109">Opis</span><span class="sxs-lookup"><span data-stu-id="09ffb-109">DESCRIPTION</span></span>
<span data-ttu-id="09ffb-110">Polecenie cmdlet **Get-AzureRmApiManagementGroup** pobiera wszystkie lub określone grupy zarządzania API.</span><span class="sxs-lookup"><span data-stu-id="09ffb-110">The **Get-AzureRmApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="09ffb-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="09ffb-111">EXAMPLES</span></span>

### <span data-ttu-id="09ffb-112">Przykład 1: pobieranie wszystkich grup</span><span class="sxs-lookup"><span data-stu-id="09ffb-112">Example 1: Get all groups</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext
```

<span data-ttu-id="09ffb-113">To polecenie pobiera wszystkie grupy.</span><span class="sxs-lookup"><span data-stu-id="09ffb-113">This command gets all groups.</span></span>

### <span data-ttu-id="09ffb-114">Przykład 2: Uzyskiwanie grupy według identyfikatorów</span><span class="sxs-lookup"><span data-stu-id="09ffb-114">Example 2: Get a group by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext -GroupId "0123456789"
```

<span data-ttu-id="09ffb-115">To polecenie pobiera identyfikator grupy o nazwie 0123456789.</span><span class="sxs-lookup"><span data-stu-id="09ffb-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="09ffb-116">Przykład 3: pobieranie grupy według nazwy</span><span class="sxs-lookup"><span data-stu-id="09ffb-116">Example 3: Get a group by name</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext -Name "Group0002"
```

<span data-ttu-id="09ffb-117">To polecenie uzyskuje grupę o nazwie Group0002.</span><span class="sxs-lookup"><span data-stu-id="09ffb-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="09ffb-118">Przykład 4: pobieranie wszystkich grup użytkowników</span><span class="sxs-lookup"><span data-stu-id="09ffb-118">Example 4: Get all user groups</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext -UserId "0123456789"
```

<span data-ttu-id="09ffb-119">To polecenie pobiera wszystkie grupy użytkowników o IDENTYFIKATORze użytkownika o nazwie 0123456789.</span><span class="sxs-lookup"><span data-stu-id="09ffb-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="09ffb-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="09ffb-120">PARAMETERS</span></span>

### <span data-ttu-id="09ffb-121">-Context</span><span class="sxs-lookup"><span data-stu-id="09ffb-121">-Context</span></span>
<span data-ttu-id="09ffb-122">Określa wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="09ffb-122">Specifies an instance of PsApiManagementContext.</span></span>

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

### <span data-ttu-id="09ffb-123">-GroupId</span><span class="sxs-lookup"><span data-stu-id="09ffb-123">-GroupId</span></span>
<span data-ttu-id="09ffb-124">Określa identyfikator grupy.</span><span class="sxs-lookup"><span data-stu-id="09ffb-124">Specifies the group ID.</span></span>
<span data-ttu-id="09ffb-125">Jeśli jest określony, polecenie cmdlet próbuje znaleźć grupę według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="09ffb-125">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by group ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09ffb-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="09ffb-126">-Name</span></span>
<span data-ttu-id="09ffb-127">Określa nazwę grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="09ffb-127">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="09ffb-128">-ProductId</span><span class="sxs-lookup"><span data-stu-id="09ffb-128">-ProductId</span></span>
<span data-ttu-id="09ffb-129">Identyfikator istniejącego produktu.</span><span class="sxs-lookup"><span data-stu-id="09ffb-129">Identifier of existing product.</span></span>
<span data-ttu-id="09ffb-130">Jeśli ta grupa zostanie wybrana, zostaną zwrócone wszystkie grupy, do których przypisano produkt.</span><span class="sxs-lookup"><span data-stu-id="09ffb-130">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="09ffb-131">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="09ffb-131">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find groups by product
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09ffb-132">-UserId</span><span class="sxs-lookup"><span data-stu-id="09ffb-132">-UserId</span></span>
<span data-ttu-id="09ffb-133">Określa identyfikator istniejącego produktu.</span><span class="sxs-lookup"><span data-stu-id="09ffb-133">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="09ffb-134">Jeśli zostanie określona, polecenie cmdlet zwróci wszystkie grupy, do których przypisano produkt.</span><span class="sxs-lookup"><span data-stu-id="09ffb-134">If specified the cmdlet will return all groups the product assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: Find groups by user
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09ffb-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09ffb-135">-DefaultProfile</span></span>
<span data-ttu-id="09ffb-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="09ffb-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09ffb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09ffb-137">CommonParameters</span></span>
<span data-ttu-id="09ffb-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09ffb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09ffb-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09ffb-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09ffb-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09ffb-140">INPUTS</span></span>

## <span data-ttu-id="09ffb-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="09ffb-141">OUTPUTS</span></span>

### <span data-ttu-id="09ffb-142">IList<Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementGroup></span><span class="sxs-lookup"><span data-stu-id="09ffb-142">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup></span></span>

## <span data-ttu-id="09ffb-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="09ffb-143">NOTES</span></span>

## <span data-ttu-id="09ffb-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="09ffb-144">RELATED LINKS</span></span>

[<span data-ttu-id="09ffb-145">Nowe — AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="09ffb-145">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="09ffb-146">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="09ffb-146">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)

[<span data-ttu-id="09ffb-147">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="09ffb-147">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


