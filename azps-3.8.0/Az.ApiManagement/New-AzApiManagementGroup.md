---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EE2BC1F7-E6F3-477D-8416-8E61893534E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGroup.md
ms.openlocfilehash: 8f7d221ca4f90f67bce038015b4c654881dfa598
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051205"
---
# <span data-ttu-id="266c3-101">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="266c3-101">New-AzApiManagementGroup</span></span>

## <span data-ttu-id="266c3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="266c3-102">SYNOPSIS</span></span>
<span data-ttu-id="266c3-103">Tworzy grupę zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="266c3-103">Creates an API management group.</span></span>

## <span data-ttu-id="266c3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="266c3-104">SYNTAX</span></span>

```
New-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] -Name <String>
 [-Description <String>] [-Type <PsApiManagementGroupType>] [-ExternalId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="266c3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="266c3-105">DESCRIPTION</span></span>
<span data-ttu-id="266c3-106">Polecenie cmdlet **New-AzApiManagementGroup** umożliwia utworzenie grupy zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="266c3-106">The **New-AzApiManagementGroup** cmdlet creates an API management group.</span></span>

## <span data-ttu-id="266c3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="266c3-107">EXAMPLES</span></span>

### <span data-ttu-id="266c3-108">Przykład 1. Tworzenie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="266c3-108">Example 1: Create a management group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementGroup -Context $apimContext -Name "Group0001"
```

<span data-ttu-id="266c3-109">To polecenie tworzy grupę zarządzania.</span><span class="sxs-lookup"><span data-stu-id="266c3-109">This command creates a management group.</span></span>

## <span data-ttu-id="266c3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="266c3-110">PARAMETERS</span></span>

### <span data-ttu-id="266c3-111">-Context</span><span class="sxs-lookup"><span data-stu-id="266c3-111">-Context</span></span>
<span data-ttu-id="266c3-112">Określa wystąpienie obiektu **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="266c3-112">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="266c3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="266c3-113">-DefaultProfile</span></span>
<span data-ttu-id="266c3-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="266c3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="266c3-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="266c3-115">-Description</span></span>
<span data-ttu-id="266c3-116">Określa opis grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="266c3-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="266c3-117">-ExternalId</span><span class="sxs-lookup"><span data-stu-id="266c3-117">-ExternalId</span></span>
<span data-ttu-id="266c3-118">W przypadku grup zewnętrznych Właściwość zawiera identyfikator grupy od dostawcy tożsamości zewnętrznej, na przykład usługę Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; w przeciwnym razie wartość jest zerowa.</span><span class="sxs-lookup"><span data-stu-id="266c3-118">For external groups, this property contains the id of the group from the external identity provider, e.g. Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; otherwise the value is null.</span></span>

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

### <span data-ttu-id="266c3-119">-GroupId</span><span class="sxs-lookup"><span data-stu-id="266c3-119">-GroupId</span></span>
<span data-ttu-id="266c3-120">Określa identyfikator nowej grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="266c3-120">Specifies the identifier of the new management group.</span></span>

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

### <span data-ttu-id="266c3-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="266c3-121">-Name</span></span>
<span data-ttu-id="266c3-122">Określa nazwę grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="266c3-122">Specifies the management group name.</span></span>

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

### <span data-ttu-id="266c3-123">-Type</span><span class="sxs-lookup"><span data-stu-id="266c3-123">-Type</span></span>
<span data-ttu-id="266c3-124">Typ grupy.</span><span class="sxs-lookup"><span data-stu-id="266c3-124">Group Type.</span></span> <span data-ttu-id="266c3-125">Grupa niestandardowa jest grupą zdefiniowaną przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="266c3-125">Custom Group is User defined Group.</span></span> <span data-ttu-id="266c3-126">Grupa systemowa obejmuje administratora, programistów i Gości.</span><span class="sxs-lookup"><span data-stu-id="266c3-126">System Group includes Administrator, Developers and Guests.</span></span> <span data-ttu-id="266c3-127">Nie można utworzyć ani zaktualizować grupy systemowej.</span><span class="sxs-lookup"><span data-stu-id="266c3-127">You cannot create or update a System Group.</span></span>  <span data-ttu-id="266c3-128">Grupa zewnętrzna to grupy z zewnętrznego dostawcy tożsamości, takie jak usługa Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="266c3-128">External Group is groups from External Identity Provider like Azure Active Directory.</span></span> <span data-ttu-id="266c3-129">Ten parametr jest opcjonalny i domyślnie przyjmowany jako Grupa niestandardowa.</span><span class="sxs-lookup"><span data-stu-id="266c3-129">This parameter is optional and by default assumed to be a Custom Group.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType]
Parameter Sets: (All)
Aliases:
Accepted values: Custom, System, External

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="266c3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="266c3-130">CommonParameters</span></span>
<span data-ttu-id="266c3-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="266c3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="266c3-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="266c3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="266c3-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="266c3-133">INPUTS</span></span>

### <span data-ttu-id="266c3-134">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="266c3-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="266c3-135">System. String</span><span class="sxs-lookup"><span data-stu-id="266c3-135">System.String</span></span>

### <span data-ttu-id="266c3-136">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. servicemanagement. modele. PsApiManagementGroupType, Microsoft. Azure. PowerShell. cmdlet. ApiManagement. servicemanagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="266c3-136">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="266c3-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="266c3-137">OUTPUTS</span></span>

### <span data-ttu-id="266c3-138">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="266c3-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="266c3-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="266c3-139">NOTES</span></span>

## <span data-ttu-id="266c3-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="266c3-140">RELATED LINKS</span></span>

[<span data-ttu-id="266c3-141">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="266c3-141">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="266c3-142">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="266c3-142">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="266c3-143">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="266c3-143">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


