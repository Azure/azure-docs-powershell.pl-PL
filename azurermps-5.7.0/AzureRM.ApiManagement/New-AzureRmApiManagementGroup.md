---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: EE2BC1F7-E6F3-477D-8416-8E61893534E2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementGroup.md
ms.openlocfilehash: 0443b9bc3ed2666600f2d119eca5b7173b21e89d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718668"
---
# <span data-ttu-id="849d0-101">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="849d0-101">New-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="849d0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="849d0-102">SYNOPSIS</span></span>
<span data-ttu-id="849d0-103">Tworzy grupę zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="849d0-103">Creates an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="849d0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="849d0-104">SYNTAX</span></span>

```
New-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] -Name <String>
 [-Description <String>] [-Type <PsApiManagementGroupType>] [-ExternalId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="849d0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="849d0-105">DESCRIPTION</span></span>
<span data-ttu-id="849d0-106">Polecenie cmdlet **New-AzureRmApiManagementGroup** umożliwia utworzenie grupy zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="849d0-106">The **New-AzureRmApiManagementGroup** cmdlet creates an API management group.</span></span>

## <span data-ttu-id="849d0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="849d0-107">EXAMPLES</span></span>

### <span data-ttu-id="849d0-108">Przykład 1. Tworzenie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="849d0-108">Example 1: Create a management group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementGroup -Context $apimContext -Name "Group0001"
```

<span data-ttu-id="849d0-109">To polecenie tworzy grupę zarządzania.</span><span class="sxs-lookup"><span data-stu-id="849d0-109">This command creates a management group.</span></span>

## <span data-ttu-id="849d0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="849d0-110">PARAMETERS</span></span>

### <span data-ttu-id="849d0-111">-Context</span><span class="sxs-lookup"><span data-stu-id="849d0-111">-Context</span></span>
<span data-ttu-id="849d0-112">Określa wystąpienie obiektu **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="849d0-112">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="849d0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="849d0-113">-DefaultProfile</span></span>
<span data-ttu-id="849d0-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="849d0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="849d0-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="849d0-115">-Description</span></span>
<span data-ttu-id="849d0-116">Określa opis grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="849d0-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="849d0-117">-ExternalId</span><span class="sxs-lookup"><span data-stu-id="849d0-117">-ExternalId</span></span>
<span data-ttu-id="849d0-118">W przypadku grup zewnętrznych Właściwość zawiera identyfikator grupy od dostawcy tożsamości zewnętrznej, na przykład usługę Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; w przeciwnym razie wartość jest zerowa.</span><span class="sxs-lookup"><span data-stu-id="849d0-118">For external groups, this property contains the id of the group from the external identity provider, e.g. Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; otherwise the value is null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="849d0-119">-GroupId</span><span class="sxs-lookup"><span data-stu-id="849d0-119">-GroupId</span></span>
<span data-ttu-id="849d0-120">Określa identyfikator nowej grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="849d0-120">Specifies the identifier of the new management group.</span></span>

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

### <span data-ttu-id="849d0-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="849d0-121">-Name</span></span>
<span data-ttu-id="849d0-122">Określa nazwę grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="849d0-122">Specifies the management group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="849d0-123">-Type</span><span class="sxs-lookup"><span data-stu-id="849d0-123">-Type</span></span>
<span data-ttu-id="849d0-124">Typ grupy.</span><span class="sxs-lookup"><span data-stu-id="849d0-124">Group Type.</span></span> <span data-ttu-id="849d0-125">Grupa niestandardowa jest grupą zdefiniowaną przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="849d0-125">Custom Group is User defined Group.</span></span> <span data-ttu-id="849d0-126">Grupa systemowa obejmuje administratora, programistów i Gości.</span><span class="sxs-lookup"><span data-stu-id="849d0-126">System Group includes Administrator, Developers and Guests.</span></span> <span data-ttu-id="849d0-127">Nie można utworzyć ani zaktualizować grupy systemowej.</span><span class="sxs-lookup"><span data-stu-id="849d0-127">You cannot create or update a System Group.</span></span>  <span data-ttu-id="849d0-128">Grupa zewnętrzna to grupy z zewnętrznego dostawcy tożsamości, takie jak usługa Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="849d0-128">External Group is groups from External Identity Provider like Azure Active Directory.</span></span> <span data-ttu-id="849d0-129">Ten parametr jest opcjonalny i domyślnie przyjmowany jako Grupa niestandardowa.</span><span class="sxs-lookup"><span data-stu-id="849d0-129">This parameter is optional and by default assumed to be a Custom Group.</span></span>

```yaml
Type: PsApiManagementGroupType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="849d0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="849d0-130">CommonParameters</span></span>
<span data-ttu-id="849d0-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="849d0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="849d0-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="849d0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="849d0-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="849d0-133">INPUTS</span></span>

### <span data-ttu-id="849d0-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="849d0-134">None</span></span>
<span data-ttu-id="849d0-135">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="849d0-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="849d0-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="849d0-136">OUTPUTS</span></span>

### <span data-ttu-id="849d0-137">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="849d0-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="849d0-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="849d0-138">NOTES</span></span>

## <span data-ttu-id="849d0-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="849d0-139">RELATED LINKS</span></span>

[<span data-ttu-id="849d0-140">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="849d0-140">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="849d0-141">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="849d0-141">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)

[<span data-ttu-id="849d0-142">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="849d0-142">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


