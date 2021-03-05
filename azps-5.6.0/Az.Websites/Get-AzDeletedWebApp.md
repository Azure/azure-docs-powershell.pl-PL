---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
ms.openlocfilehash: a67e48cdcad9d80d244e74ef8e20f81fcbd157cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983889"
---
# <span data-ttu-id="d9fdb-101">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="d9fdb-101">Get-AzDeletedWebApp</span></span>

## <span data-ttu-id="d9fdb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9fdb-102">SYNOPSIS</span></span>
<span data-ttu-id="d9fdb-103">Usuwa aplikacje sieci Web z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d9fdb-103">Gets deleted web apps in the subscription.</span></span>

## <span data-ttu-id="d9fdb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d9fdb-104">SYNTAX</span></span>

```
Get-AzDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9fdb-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d9fdb-105">DESCRIPTION</span></span>
<span data-ttu-id="d9fdb-106">Polecenie **cmdlet Get-AzDeletedWebApp** zwraca wszystkie usunięte aplikacje sieci Web w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d9fdb-106">The **Get-AzDeletedWebApp** cmdlet returns all deleted web apps in the subscription.</span></span> <span data-ttu-id="d9fdb-107">Usunięte aplikacje można opcjonalnie filtrować według grupy zasobów, nazwy i miejsca.</span><span class="sxs-lookup"><span data-stu-id="d9fdb-107">Deleted apps can optionally be filtered by resource group, name, and slot.</span></span> <span data-ttu-id="d9fdb-108">Może być więcej niż jedna usunięta aplikacja o tej samej nazwie i grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="d9fdb-108">There can be more than one deleted app with the same name and resource group.</span></span> <span data-ttu-id="d9fdb-109">Sprawdź czas usunięcia, aby odróżnić usunięte aplikacje o tej samej nazwie.</span><span class="sxs-lookup"><span data-stu-id="d9fdb-109">Check the DeletionTime to distinguish deleted apps that share the same name.</span></span>

## <span data-ttu-id="d9fdb-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d9fdb-110">EXAMPLES</span></span>

### <span data-ttu-id="d9fdb-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d9fdb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="d9fdb-112">To polecenie pobiera usunięte aplikacje o nazwie ContosoSite należące do grupy zasobów Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="d9fdb-112">This command gets the deleted apps named ContosoSite belonging to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="d9fdb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9fdb-113">PARAMETERS</span></span>

### <span data-ttu-id="d9fdb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9fdb-114">-DefaultProfile</span></span>
<span data-ttu-id="d9fdb-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9fdb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9fdb-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d9fdb-116">-Location</span></span>
<span data-ttu-id="d9fdb-117">Lokalizacja usuniętej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d9fdb-117">The location of the deleted app.</span></span>

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

### <span data-ttu-id="d9fdb-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d9fdb-118">-Name</span></span>
<span data-ttu-id="d9fdb-119">Nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="d9fdb-119">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9fdb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9fdb-120">-ResourceGroupName</span></span>
<span data-ttu-id="d9fdb-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d9fdb-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9fdb-122">— Slot</span><span class="sxs-lookup"><span data-stu-id="d9fdb-122">-Slot</span></span>
<span data-ttu-id="d9fdb-123">Nazwa miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="d9fdb-123">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9fdb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9fdb-124">CommonParameters</span></span>
<span data-ttu-id="d9fdb-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9fdb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9fdb-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9fdb-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9fdb-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9fdb-127">INPUTS</span></span>

### <span data-ttu-id="d9fdb-128">Brak</span><span class="sxs-lookup"><span data-stu-id="d9fdb-128">None</span></span>

## <span data-ttu-id="d9fdb-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9fdb-129">OUTPUTS</span></span>

### <span data-ttu-id="d9fdb-130">Microsoft.Azure.Commands.WebApps.Cmdlet.WebApps.PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="d9fdb-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="d9fdb-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d9fdb-131">NOTES</span></span>

## <span data-ttu-id="d9fdb-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9fdb-132">RELATED LINKS</span></span>

[<span data-ttu-id="d9fdb-133">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="d9fdb-133">Restore-AzDeletedWebApp</span></span>](./Restore-AzDeletedWebApp.md)