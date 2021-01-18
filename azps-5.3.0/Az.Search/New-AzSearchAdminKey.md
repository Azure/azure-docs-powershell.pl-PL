---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchadminkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchAdminKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchAdminKey.md
ms.openlocfilehash: ae925d39dab3b56e70cb7c42b320e57eb7f7811a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498430"
---
# <span data-ttu-id="6411c-101">New-AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="6411c-101">New-AzSearchAdminKey</span></span>

## <span data-ttu-id="6411c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6411c-102">SYNOPSIS</span></span>
<span data-ttu-id="6411c-103">Generuje ponownie klucz administrator usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="6411c-103">Regenerates an admin key of the Azure Search service.</span></span>

## <span data-ttu-id="6411c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6411c-104">SYNTAX</span></span>

### <span data-ttu-id="6411c-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6411c-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchAdminKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyKind <PSSearchAdminKeyKind>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6411c-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6411c-106">ParentObjectParameterSet</span></span>
```
New-AzSearchAdminKey [-ParentObject] <PSSearchService> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6411c-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6411c-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchAdminKey [-ParentResourceId] <String> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6411c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6411c-108">DESCRIPTION</span></span>
<span data-ttu-id="6411c-109">Polecenie cmdlet **New-AzSearchAdminKey** generuje klucz administrator usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="6411c-109">The **New-AzSearchAdminKey** cmdlet regenerates an admin key of the Azure Search service.</span></span>

## <span data-ttu-id="6411c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6411c-110">EXAMPLES</span></span>

### <span data-ttu-id="6411c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6411c-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchAdminKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyKind Primary

Confirm
Are you sure you want to regenerate 'Primary' key for Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

Primary                          Secondary
-------                          ---------
85B3813D11904B591BE8A196C2C743A1 CEF791D5BAC2E6C0B232C56702F21E87
```

<span data-ttu-id="6411c-112">Ten przykład generuje klucz podstawowy usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="6411c-112">The example regenerates Primary key of the Azure Search Service.</span></span>

## <span data-ttu-id="6411c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6411c-113">PARAMETERS</span></span>

### <span data-ttu-id="6411c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6411c-114">-DefaultProfile</span></span>
<span data-ttu-id="6411c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6411c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6411c-116">-Force</span><span class="sxs-lookup"><span data-stu-id="6411c-116">-Force</span></span>
<span data-ttu-id="6411c-117">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6411c-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6411c-118">-Rodzaj</span><span class="sxs-lookup"><span data-stu-id="6411c-118">-KeyKind</span></span>
<span data-ttu-id="6411c-119">Rodzaj klucza administratora usługi wyszukiwania (podstawowy/pomocniczy).</span><span class="sxs-lookup"><span data-stu-id="6411c-119">Search Service admin key kind (Primary/Secondary).</span></span>

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

### <span data-ttu-id="6411c-120">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="6411c-120">-ParentObject</span></span>
<span data-ttu-id="6411c-121">Obiekt wejściowy usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="6411c-121">Search Service Input Object.</span></span>

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

### <span data-ttu-id="6411c-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6411c-122">-ParentResourceId</span></span>
<span data-ttu-id="6411c-123">Identyfikator zasobu usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="6411c-123">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="6411c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6411c-124">-ResourceGroupName</span></span>
<span data-ttu-id="6411c-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6411c-125">Resource Group name.</span></span>

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

### <span data-ttu-id="6411c-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6411c-126">-ServiceName</span></span>
<span data-ttu-id="6411c-127">Nazwa usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="6411c-127">Search Service name.</span></span>

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

### <span data-ttu-id="6411c-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6411c-128">-Confirm</span></span>
<span data-ttu-id="6411c-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6411c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6411c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6411c-130">-WhatIf</span></span>
<span data-ttu-id="6411c-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6411c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6411c-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6411c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6411c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6411c-133">CommonParameters</span></span>
<span data-ttu-id="6411c-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6411c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6411c-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6411c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6411c-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6411c-136">INPUTS</span></span>

### <span data-ttu-id="6411c-137">Microsoft. Azure. Commands. Management. Search. Search. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="6411c-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="6411c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6411c-138">System.String</span></span>

## <span data-ttu-id="6411c-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6411c-139">OUTPUTS</span></span>

### <span data-ttu-id="6411c-140">Microsoft. Azure. Commands. Management. Search. Search. PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="6411c-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="6411c-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6411c-141">NOTES</span></span>

## <span data-ttu-id="6411c-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6411c-142">RELATED LINKS</span></span>

[<span data-ttu-id="6411c-143">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="6411c-143">Get-AzSearchAdminKeyPair</span></span>](./Get-AzSearchAdminKeyPair.md)
