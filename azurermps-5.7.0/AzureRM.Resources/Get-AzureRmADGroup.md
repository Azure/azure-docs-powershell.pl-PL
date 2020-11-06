---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
ms.openlocfilehash: 29c3a76817bd50a5f86ea051b6de1139980a0dba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550580"
---
# <span data-ttu-id="6a938-101">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="6a938-101">Get-AzureRmADGroup</span></span>

## <span data-ttu-id="6a938-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6a938-102">SYNOPSIS</span></span>
<span data-ttu-id="6a938-103">Umożliwia filtrowanie grup usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6a938-103">Filters active directory groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a938-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6a938-104">SYNTAX</span></span>

### <span data-ttu-id="6a938-105">EmptyParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6a938-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a938-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a938-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADGroup -SearchString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a938-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a938-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a938-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6a938-108">DESCRIPTION</span></span>
<span data-ttu-id="6a938-109">Umożliwia filtrowanie grup usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6a938-109">Filters active directory groups.</span></span>

## <span data-ttu-id="6a938-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6a938-110">EXAMPLES</span></span>

### <span data-ttu-id="6a938-111">Filtrowanie grup przy użyciu identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="6a938-111">Filters groups using object id</span></span>
```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="6a938-112">Pobiera grupę z identyfikatorem 85F89C90-780E-4AA6-9F4F-6F268D322EEE</span><span class="sxs-lookup"><span data-stu-id="6a938-112">Gets group with 85F89C90-780E-4AA6-9F4F-6F268D322EEE id</span></span>

### <span data-ttu-id="6a938-113">Filtruje grupy przy użyciu ciągu wyszukiwania</span><span class="sxs-lookup"><span data-stu-id="6a938-113">Filters groups using Search String</span></span>
```
PS C:\> Get-AzureRmADGroup -SearchString Joe
```

<span data-ttu-id="6a938-114">Filtruje wszystkie grupy usługi AD, które mają Janusza, w nazwie wyświetlanej.</span><span class="sxs-lookup"><span data-stu-id="6a938-114">Filters all ad groups that has Joe in the display name.</span></span>

### <span data-ttu-id="6a938-115">Lista grup usługi AD</span><span class="sxs-lookup"><span data-stu-id="6a938-115">List AD groups</span></span>
```
PS C:\> Get-AzureRmADGroup
```

<span data-ttu-id="6a938-116">Pobiera wszystkie grupy usługi AD</span><span class="sxs-lookup"><span data-stu-id="6a938-116">Gets all AD groups</span></span>

## <span data-ttu-id="6a938-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6a938-117">PARAMETERS</span></span>

### <span data-ttu-id="6a938-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a938-118">-DefaultProfile</span></span>
<span data-ttu-id="6a938-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6a938-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6a938-120">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="6a938-120">-ObjectId</span></span>
<span data-ttu-id="6a938-121">Identyfikator obiektu grupy.</span><span class="sxs-lookup"><span data-stu-id="6a938-121">Object id of the group.</span></span>

```yaml
Type: Guid
Parameter Sets: EmptyParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a938-122">-SearchString</span><span class="sxs-lookup"><span data-stu-id="6a938-122">-SearchString</span></span>
<span data-ttu-id="6a938-123">Nazwa wyświetlana grupy</span><span class="sxs-lookup"><span data-stu-id="6a938-123">The group display name</span></span>

```yaml
Type: String
Parameter Sets: SearchStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a938-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a938-124">CommonParameters</span></span>
<span data-ttu-id="6a938-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a938-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a938-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a938-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a938-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a938-127">INPUTS</span></span>

### <span data-ttu-id="6a938-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6a938-128">None</span></span>
<span data-ttu-id="6a938-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="6a938-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6a938-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6a938-130">OUTPUTS</span></span>

### <span data-ttu-id="6a938-131">System. Collections. Generic. list "1 [Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADGroup]</span><span class="sxs-lookup"><span data-stu-id="6a938-131">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup]</span></span>

## <span data-ttu-id="6a938-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6a938-132">NOTES</span></span>

## <span data-ttu-id="6a938-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a938-133">RELATED LINKS</span></span>

[<span data-ttu-id="6a938-134">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="6a938-134">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="6a938-135">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6a938-135">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="6a938-136">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="6a938-136">Get-AzureRmADGroupMember</span></span>](./Get-AzureRmADGroupMember.md)

