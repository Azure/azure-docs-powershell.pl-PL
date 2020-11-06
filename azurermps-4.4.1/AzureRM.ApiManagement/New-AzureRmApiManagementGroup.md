---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: EE2BC1F7-E6F3-477D-8416-8E61893534E2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementGroup.md
ms.openlocfilehash: 8fc237b130e5044e52f47d306d04c42d12fbad81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547207"
---
# <span data-ttu-id="1a67d-101">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="1a67d-101">New-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="1a67d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1a67d-102">SYNOPSIS</span></span>
<span data-ttu-id="1a67d-103">Tworzy grupę zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="1a67d-103">Creates an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a67d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1a67d-104">SYNTAX</span></span>

```
New-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] -Name <String>
 [-Description <String>] [-Type <PsApiManagementGroupType>] [-ExternalId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a67d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1a67d-105">DESCRIPTION</span></span>
<span data-ttu-id="1a67d-106">Polecenie cmdlet **New-AzureRmApiManagementGroup** umożliwia utworzenie grupy zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="1a67d-106">The **New-AzureRmApiManagementGroup** cmdlet creates an API management group.</span></span>

## <span data-ttu-id="1a67d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1a67d-107">EXAMPLES</span></span>

### <span data-ttu-id="1a67d-108">Przykład 1. Tworzenie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="1a67d-108">Example 1: Create a management group</span></span>
```
PS C:\>New-AzureRmApiManagementGroup -Context $APImContext -Name "Group0001"
```

<span data-ttu-id="1a67d-109">To polecenie tworzy grupę zarządzania.</span><span class="sxs-lookup"><span data-stu-id="1a67d-109">This command creates a management group.</span></span>

## <span data-ttu-id="1a67d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1a67d-110">PARAMETERS</span></span>

### <span data-ttu-id="1a67d-111">-Context</span><span class="sxs-lookup"><span data-stu-id="1a67d-111">-Context</span></span>
<span data-ttu-id="1a67d-112">Określa wystąpienie obiektu **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="1a67d-112">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1a67d-113">— Opis</span><span class="sxs-lookup"><span data-stu-id="1a67d-113">-Description</span></span>
<span data-ttu-id="1a67d-114">Określa opis grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="1a67d-114">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="1a67d-115">-ExternalId</span><span class="sxs-lookup"><span data-stu-id="1a67d-115">-ExternalId</span></span>
<span data-ttu-id="1a67d-116">W przypadku grup zewnętrznych Właściwość zawiera identyfikator grupy od dostawcy tożsamości zewnętrznej, na przykład usługę Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; w przeciwnym razie wartość jest zerowa.</span><span class="sxs-lookup"><span data-stu-id="1a67d-116">For external groups, this property contains the id of the group from the external identity provider, e.g. Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; otherwise the value is null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a67d-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="1a67d-117">-GroupId</span></span>
<span data-ttu-id="1a67d-118">Określa identyfikator nowej grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="1a67d-118">Specifies the identifier of the new management group.</span></span>

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

### <span data-ttu-id="1a67d-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1a67d-119">-Name</span></span>
<span data-ttu-id="1a67d-120">Określa nazwę grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="1a67d-120">Specifies the management group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a67d-121">-Type</span><span class="sxs-lookup"><span data-stu-id="1a67d-121">-Type</span></span>
<span data-ttu-id="1a67d-122">Typ grupy.</span><span class="sxs-lookup"><span data-stu-id="1a67d-122">Group Type.</span></span> <span data-ttu-id="1a67d-123">Grupa niestandardowa jest grupą zdefiniowaną przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1a67d-123">Custom Group is User defined Group.</span></span> <span data-ttu-id="1a67d-124">Grupa systemowa obejmuje administratora, programistów i Gości.</span><span class="sxs-lookup"><span data-stu-id="1a67d-124">System Group includes Administrator, Developers and Guests.</span></span> <span data-ttu-id="1a67d-125">Nie można utworzyć ani zaktualizować grupy systemowej.</span><span class="sxs-lookup"><span data-stu-id="1a67d-125">You cannot create or update a System Group.</span></span>  <span data-ttu-id="1a67d-126">Grupa zewnętrzna to grupy z zewnętrznego dostawcy tożsamości, takie jak usługa Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1a67d-126">External Group is groups from External Identity Provider like Azure Active Directory.</span></span> <span data-ttu-id="1a67d-127">Ten parametr jest opcjonalny i domyślnie przyjmowany jako Grupa niestandardowa.</span><span class="sxs-lookup"><span data-stu-id="1a67d-127">This parameter is optional and by default assumed to be a Custom Group.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a67d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a67d-128">-DefaultProfile</span></span>
<span data-ttu-id="1a67d-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1a67d-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a67d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a67d-130">CommonParameters</span></span>
<span data-ttu-id="1a67d-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a67d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a67d-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a67d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a67d-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a67d-133">INPUTS</span></span>

## <span data-ttu-id="1a67d-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1a67d-134">OUTPUTS</span></span>

### <span data-ttu-id="1a67d-135">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="1a67d-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="1a67d-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1a67d-136">NOTES</span></span>

## <span data-ttu-id="1a67d-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1a67d-137">RELATED LINKS</span></span>

[<span data-ttu-id="1a67d-138">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="1a67d-138">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="1a67d-139">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="1a67d-139">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)

[<span data-ttu-id="1a67d-140">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="1a67d-140">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


