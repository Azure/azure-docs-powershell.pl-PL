---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: 350f7d5b44f5a1c84f97511a4febb7d967ee2de4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242938"
---
# <span data-ttu-id="c13df-101">Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="c13df-101">Get-AzWebAppSnapshot</span></span>

## <span data-ttu-id="c13df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c13df-102">SYNOPSIS</span></span>
<span data-ttu-id="c13df-103">Pobiera migawki dostępne dla aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="c13df-103">Gets the snapshots available for a web app.</span></span>

## <span data-ttu-id="c13df-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c13df-104">SYNTAX</span></span>

### <span data-ttu-id="c13df-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="c13df-105">FromResourceName</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c13df-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="c13df-106">FromWebApp</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c13df-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c13df-107">DESCRIPTION</span></span>
<span data-ttu-id="c13df-108">Polecenie **cmdlet Get-AzWebAppSnapshot** zwraca wszystkie migawki aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="c13df-108">The **Get-AzWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="c13df-109">Migawki to automatyczne kopie zapasowe plików i ustawień aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="c13df-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="c13df-110">Migawkę można przywrócić za pomocą polecenia cmdlet **Restore-AzWebAppSnapshot.**</span><span class="sxs-lookup"><span data-stu-id="c13df-110">A snapshot can be restored with the **Restore-AzWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="c13df-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c13df-111">EXAMPLES</span></span>

### <span data-ttu-id="c13df-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c13df-112">Example 1</span></span>
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="c13df-113">Uzyskiwanie migawek aplikacji sieci Web o nazwie "ContosoApp" z slotem o nazwie "Tymczasowe" w grupie zasobów "Default-Web-WestUS"</span><span class="sxs-lookup"><span data-stu-id="c13df-113">Get the snapshots for a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="c13df-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c13df-114">PARAMETERS</span></span>

### <span data-ttu-id="c13df-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c13df-115">-DefaultProfile</span></span>
<span data-ttu-id="c13df-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c13df-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c13df-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c13df-117">-Name</span></span>
<span data-ttu-id="c13df-118">Nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="c13df-118">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c13df-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c13df-119">-ResourceGroupName</span></span>
<span data-ttu-id="c13df-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c13df-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c13df-121">— Slot</span><span class="sxs-lookup"><span data-stu-id="c13df-121">-Slot</span></span>
<span data-ttu-id="c13df-122">Nazwa miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="c13df-122">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c13df-123">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="c13df-123">-UseDisasterRecovery</span></span>
<span data-ttu-id="c13df-124">Odczytywanie migawek jednostki pomocniczej skali.</span><span class="sxs-lookup"><span data-stu-id="c13df-124">Read the snapshots from a secondary scale unit.</span></span>

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

### <span data-ttu-id="c13df-125">- WebApp</span><span class="sxs-lookup"><span data-stu-id="c13df-125">-WebApp</span></span>
<span data-ttu-id="c13df-126">Obiekt aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="c13df-126">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c13df-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c13df-127">CommonParameters</span></span>
<span data-ttu-id="c13df-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c13df-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c13df-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c13df-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c13df-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c13df-130">INPUTS</span></span>

### <span data-ttu-id="c13df-131">System.String</span><span class="sxs-lookup"><span data-stu-id="c13df-131">System.String</span></span>

### <span data-ttu-id="c13df-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="c13df-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c13df-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c13df-133">OUTPUTS</span></span>

### <span data-ttu-id="c13df-134">Microsoft.Azure.Commands.WebApps.Cmdlet.BackupRestore.AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="c13df-134">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="c13df-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c13df-135">NOTES</span></span>

## <span data-ttu-id="c13df-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c13df-136">RELATED LINKS</span></span>
