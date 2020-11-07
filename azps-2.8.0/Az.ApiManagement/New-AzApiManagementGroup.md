---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EE2BC1F7-E6F3-477D-8416-8E61893534E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGroup.md
ms.openlocfilehash: d55d68a6154f5f960063156578e8446777918ea9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707012"
---
# <span data-ttu-id="a74a4-101">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a74a4-101">New-AzApiManagementGroup</span></span>

## <span data-ttu-id="a74a4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a74a4-102">SYNOPSIS</span></span>
<span data-ttu-id="a74a4-103">Tworzy grupę zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="a74a4-103">Creates an API management group.</span></span>

## <span data-ttu-id="a74a4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a74a4-104">SYNTAX</span></span>

```
New-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] -Name <String>
 [-Description <String>] [-Type <PsApiManagementGroupType>] [-ExternalId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a74a4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a74a4-105">DESCRIPTION</span></span>
<span data-ttu-id="a74a4-106">Polecenie cmdlet **New-AzApiManagementGroup** umożliwia utworzenie grupy zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="a74a4-106">The **New-AzApiManagementGroup** cmdlet creates an API management group.</span></span>

## <span data-ttu-id="a74a4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a74a4-107">EXAMPLES</span></span>

### <span data-ttu-id="a74a4-108">Przykład 1. Tworzenie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="a74a4-108">Example 1: Create a management group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementGroup -Context $apimContext -Name "Group0001"
```

<span data-ttu-id="a74a4-109">To polecenie tworzy grupę zarządzania.</span><span class="sxs-lookup"><span data-stu-id="a74a4-109">This command creates a management group.</span></span>

## <span data-ttu-id="a74a4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a74a4-110">PARAMETERS</span></span>

### <span data-ttu-id="a74a4-111">-Context</span><span class="sxs-lookup"><span data-stu-id="a74a4-111">-Context</span></span>
<span data-ttu-id="a74a4-112">Określa wystąpienie obiektu **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="a74a4-112">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a74a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a74a4-113">-DefaultProfile</span></span>
<span data-ttu-id="a74a4-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a74a4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a74a4-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="a74a4-115">-Description</span></span>
<span data-ttu-id="a74a4-116">Określa opis grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="a74a4-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="a74a4-117">-ExternalId</span><span class="sxs-lookup"><span data-stu-id="a74a4-117">-ExternalId</span></span>
<span data-ttu-id="a74a4-118">W przypadku grup zewnętrznych Właściwość zawiera identyfikator grupy od dostawcy tożsamości zewnętrznej, na przykład usługę Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; w przeciwnym razie wartość jest zerowa.</span><span class="sxs-lookup"><span data-stu-id="a74a4-118">For external groups, this property contains the id of the group from the external identity provider, e.g. Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; otherwise the value is null.</span></span>

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

### <span data-ttu-id="a74a4-119">-GroupId</span><span class="sxs-lookup"><span data-stu-id="a74a4-119">-GroupId</span></span>
<span data-ttu-id="a74a4-120">Określa identyfikator nowej grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="a74a4-120">Specifies the identifier of the new management group.</span></span>

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

### <span data-ttu-id="a74a4-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a74a4-121">-Name</span></span>
<span data-ttu-id="a74a4-122">Określa nazwę grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="a74a4-122">Specifies the management group name.</span></span>

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

### <span data-ttu-id="a74a4-123">-Type</span><span class="sxs-lookup"><span data-stu-id="a74a4-123">-Type</span></span>
<span data-ttu-id="a74a4-124">Typ grupy.</span><span class="sxs-lookup"><span data-stu-id="a74a4-124">Group Type.</span></span> <span data-ttu-id="a74a4-125">Grupa niestandardowa jest grupą zdefiniowaną przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a74a4-125">Custom Group is User defined Group.</span></span> <span data-ttu-id="a74a4-126">Grupa systemowa obejmuje administratora, programistów i Gości.</span><span class="sxs-lookup"><span data-stu-id="a74a4-126">System Group includes Administrator, Developers and Guests.</span></span> <span data-ttu-id="a74a4-127">Nie można utworzyć ani zaktualizować grupy systemowej.</span><span class="sxs-lookup"><span data-stu-id="a74a4-127">You cannot create or update a System Group.</span></span>  <span data-ttu-id="a74a4-128">Grupa zewnętrzna to grupy z zewnętrznego dostawcy tożsamości, takie jak usługa Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a74a4-128">External Group is groups from External Identity Provider like Azure Active Directory.</span></span> <span data-ttu-id="a74a4-129">Ten parametr jest opcjonalny i domyślnie przyjmowany jako Grupa niestandardowa.</span><span class="sxs-lookup"><span data-stu-id="a74a4-129">This parameter is optional and by default assumed to be a Custom Group.</span></span>

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

### <span data-ttu-id="a74a4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a74a4-130">CommonParameters</span></span>
<span data-ttu-id="a74a4-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a74a4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a74a4-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a74a4-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a74a4-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a74a4-133">INPUTS</span></span>

### <span data-ttu-id="a74a4-134">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a74a4-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a74a4-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a74a4-135">System.String</span></span>

### <span data-ttu-id="a74a4-136">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. servicemanagement. modele. PsApiManagementGroupType, Microsoft. Azure. PowerShell. cmdlet. ApiManagement. servicemanagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a74a4-136">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a74a4-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a74a4-137">OUTPUTS</span></span>

### <span data-ttu-id="a74a4-138">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a74a4-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="a74a4-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a74a4-139">NOTES</span></span>

## <span data-ttu-id="a74a4-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a74a4-140">RELATED LINKS</span></span>

[<span data-ttu-id="a74a4-141">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a74a4-141">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="a74a4-142">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a74a4-142">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="a74a4-143">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a74a4-143">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


