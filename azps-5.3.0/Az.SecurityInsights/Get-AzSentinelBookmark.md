---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelBookmark.md
ms.openlocfilehash: 53dfedcfe4e61deb5064b20134bf063921532aec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502983"
---
# <span data-ttu-id="a4d1d-101">Get-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="a4d1d-101">Get-AzSentinelBookmark</span></span>

## <span data-ttu-id="a4d1d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a4d1d-102">SYNOPSIS</span></span>
<span data-ttu-id="a4d1d-103">Uzyskaj zakładkę.</span><span class="sxs-lookup"><span data-stu-id="a4d1d-103">Get a Bookmark.</span></span>

## <span data-ttu-id="a4d1d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a4d1d-104">SYNTAX</span></span>

### <span data-ttu-id="a4d1d-105">WorkspaceScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a4d1d-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4d1d-106">BookmarkId.</span><span class="sxs-lookup"><span data-stu-id="a4d1d-106">BookmarkId.</span></span>
```
Get-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4d1d-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="a4d1d-107">ResourceId</span></span>
```
Get-AzSentinelBookmark -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4d1d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a4d1d-108">DESCRIPTION</span></span>
<span data-ttu-id="a4d1d-109">Polecenie cmdlet **Get-AzSentinelBookmark** pobiera zakładkę z określonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="a4d1d-109">The **Get-AzSentinelBookmark** cmdlet gets a Bookmark from the specified workspace.</span></span>
<span data-ttu-id="a4d1d-110">Jeśli określisz parametr *BookmarkId* , zostanie zwrócony jeden obiekt **Bookmark** .</span><span class="sxs-lookup"><span data-stu-id="a4d1d-110">If you specify the *BookmarkId* parameter, a single **Bookmark** object is returned.</span></span>
<span data-ttu-id="a4d1d-111">Jeśli nie określisz parametru *BookmarkId* , zostanie zwrócona tablica zawierająca wszystkie zakładki w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="a4d1d-111">If you do not specify the *BookmarkId* parameter, an array containing all of the Bookmarks in the specified workspace are returned.</span></span>
<span data-ttu-id="a4d1d-112">Możesz użyć obiektu **zakładka** , aby zaktualizować zakładkę, na przykład możesz dodać notatki za pomocą **zakładki**.</span><span class="sxs-lookup"><span data-stu-id="a4d1d-112">You can use the **Bookmark** object to update the Bookmark, for example you can add Notes the **Bookmark**.</span></span>

## <span data-ttu-id="a4d1d-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a4d1d-113">EXAMPLES</span></span>

### <span data-ttu-id="a4d1d-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a4d1d-114">Example 1</span></span>
```powershell
PS C:\> $Bookmarks = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="a4d1d-115">Ten przykład powoduje wyświetlenie wszystkich **zakładek** w określonym obszarze roboczym, a następnie zapisanie go w zmiennej $Bookmarks.</span><span class="sxs-lookup"><span data-stu-id="a4d1d-115">This example gets all of the **Bookmarks** in the specified workspace, and then stores it in the $Bookmarks variable.</span></span>

### <span data-ttu-id="a4d1d-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a4d1d-116">Example 2</span></span>
```powershell
PS C:\> $Bookmark = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -BookmarkId "MyBookmarkId"
```

<span data-ttu-id="a4d1d-117">W tym przykładzie jest pobierana **zakładka** w określonym obszarze roboczym, a następnie jest ona umieszczana w zmiennej $Bookmark.</span><span class="sxs-lookup"><span data-stu-id="a4d1d-117">This example gets an **Bookmark** in the specified workspace, and then stores it in the $Bookmark variable.</span></span>

## <span data-ttu-id="a4d1d-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a4d1d-118">PARAMETERS</span></span>

### <span data-ttu-id="a4d1d-119">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="a4d1d-119">-BookmarkId</span></span>
<span data-ttu-id="a4d1d-120">Identyfikator zakładki,</span><span class="sxs-lookup"><span data-stu-id="a4d1d-120">Bookmark Id,</span></span>

```yaml
Type: System.String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4d1d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4d1d-121">-DefaultProfile</span></span>
<span data-ttu-id="a4d1d-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a4d1d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4d1d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4d1d-123">-ResourceGroupName</span></span>
<span data-ttu-id="a4d1d-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a4d1d-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4d1d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4d1d-125">-ResourceId</span></span>
<span data-ttu-id="a4d1d-126">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="a4d1d-126">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4d1d-127">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="a4d1d-127">-WorkspaceName</span></span>
<span data-ttu-id="a4d1d-128">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="a4d1d-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4d1d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4d1d-129">CommonParameters</span></span>
<span data-ttu-id="a4d1d-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4d1d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4d1d-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4d1d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4d1d-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4d1d-132">INPUTS</span></span>

### <span data-ttu-id="a4d1d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a4d1d-133">System.String</span></span>
## <span data-ttu-id="a4d1d-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a4d1d-134">OUTPUTS</span></span>

### <span data-ttu-id="a4d1d-135">Microsoft. Azure. Commands. SecurityInsights. models. zakładki. PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="a4d1d-135">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="a4d1d-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a4d1d-136">NOTES</span></span>

## <span data-ttu-id="a4d1d-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4d1d-137">RELATED LINKS</span></span>
