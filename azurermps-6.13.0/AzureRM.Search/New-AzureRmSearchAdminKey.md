---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/new-azurermsearchadminkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchAdminKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchAdminKey.md
ms.openlocfilehash: fa7ea6f1e53b94a349d51856432f1c01b2e89ba0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717601"
---
# <span data-ttu-id="a25bc-101">New-AzureRmSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="a25bc-101">New-AzureRmSearchAdminKey</span></span>

## <span data-ttu-id="a25bc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a25bc-102">SYNOPSIS</span></span>
<span data-ttu-id="a25bc-103">Generuje ponownie klucz administrator usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="a25bc-103">Regenerates an admin key of the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a25bc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a25bc-104">SYNTAX</span></span>

### <span data-ttu-id="a25bc-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a25bc-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzureRmSearchAdminKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyKind <PSSearchAdminKeyKind>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a25bc-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a25bc-106">ParentObjectParameterSet</span></span>
```
New-AzureRmSearchAdminKey [-ParentObject] <PSSearchService> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a25bc-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a25bc-107">ParentResourceIdParameterSet</span></span>
```
New-AzureRmSearchAdminKey [-ParentResourceId] <String> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a25bc-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a25bc-108">DESCRIPTION</span></span>
<span data-ttu-id="a25bc-109">Polecenie cmdlet **New-AzureRmSearchAdminKey** generuje klucz administrator usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="a25bc-109">The **New-AzureRmSearchAdminKey** cmdlet regenerates an admin key of the Azure Search service.</span></span>

## <span data-ttu-id="a25bc-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a25bc-110">EXAMPLES</span></span>

### <span data-ttu-id="a25bc-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a25bc-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSearchAdminKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyKind Primary

Confirm
Are you sure you want to regenerate 'Primary' key for Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

Primary                          Secondary
-------                          ---------
85B3813D11904B591BE8A196C2C743A1 CEF791D5BAC2E6C0B232C56702F21E87
```

<span data-ttu-id="a25bc-112">Ten przykład generuje klucz podstawowy usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="a25bc-112">The example regenerates Primary key of the Azure Search Service.</span></span>

## <span data-ttu-id="a25bc-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a25bc-113">PARAMETERS</span></span>

### <span data-ttu-id="a25bc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a25bc-114">-DefaultProfile</span></span>
<span data-ttu-id="a25bc-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a25bc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a25bc-116">-Force</span><span class="sxs-lookup"><span data-stu-id="a25bc-116">-Force</span></span>
<span data-ttu-id="a25bc-117">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a25bc-117">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25bc-118">-Rodzaj</span><span class="sxs-lookup"><span data-stu-id="a25bc-118">-KeyKind</span></span>
<span data-ttu-id="a25bc-119">Rodzaj klucza administratora usługi wyszukiwania (podstawowy/pomocniczy).</span><span class="sxs-lookup"><span data-stu-id="a25bc-119">Search Service admin key kind (Primary/Secondary).</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKeyKind
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25bc-120">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="a25bc-120">-ParentObject</span></span>
<span data-ttu-id="a25bc-121">Obiekt wejściowy usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="a25bc-121">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a25bc-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a25bc-122">-ParentResourceId</span></span>
<span data-ttu-id="a25bc-123">Identyfikator zasobu usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="a25bc-123">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a25bc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a25bc-124">-ResourceGroupName</span></span>
<span data-ttu-id="a25bc-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a25bc-125">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25bc-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a25bc-126">-ServiceName</span></span>
<span data-ttu-id="a25bc-127">Nazwa usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="a25bc-127">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25bc-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a25bc-128">-Confirm</span></span>
<span data-ttu-id="a25bc-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a25bc-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25bc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a25bc-130">-WhatIf</span></span>
<span data-ttu-id="a25bc-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a25bc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a25bc-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a25bc-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25bc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a25bc-133">CommonParameters</span></span>
<span data-ttu-id="a25bc-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a25bc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a25bc-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a25bc-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a25bc-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a25bc-136">INPUTS</span></span>

### <span data-ttu-id="a25bc-137">Microsoft. Azure. Commands. Management. Search. Search. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="a25bc-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="a25bc-138">Parametry: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a25bc-138">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="a25bc-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a25bc-139">System.String</span></span>

## <span data-ttu-id="a25bc-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a25bc-140">OUTPUTS</span></span>

### <span data-ttu-id="a25bc-141">Microsoft. Azure. Commands. Management. Search. Search. PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="a25bc-141">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="a25bc-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a25bc-142">NOTES</span></span>

## <span data-ttu-id="a25bc-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a25bc-143">RELATED LINKS</span></span>

[<span data-ttu-id="a25bc-144">Get-AzureRmSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="a25bc-144">Get-AzureRmSearchAdminKeyPair</span></span>](./Get-AzureRmSearchAdminKeyPair.md)
