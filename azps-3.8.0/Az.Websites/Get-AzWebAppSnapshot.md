---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: 350f7d5b44f5a1c84f97511a4febb7d967ee2de4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050811"
---
# <span data-ttu-id="23aed-101">Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="23aed-101">Get-AzWebAppSnapshot</span></span>

## <span data-ttu-id="23aed-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="23aed-102">SYNOPSIS</span></span>
<span data-ttu-id="23aed-103">Pobiera migawki dostępne dla aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="23aed-103">Gets the snapshots available for a web app.</span></span>

## <span data-ttu-id="23aed-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="23aed-104">SYNTAX</span></span>

### <span data-ttu-id="23aed-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="23aed-105">FromResourceName</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23aed-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="23aed-106">FromWebApp</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="23aed-107">Opis</span><span class="sxs-lookup"><span data-stu-id="23aed-107">DESCRIPTION</span></span>
<span data-ttu-id="23aed-108">Polecenie cmdlet **Get-AzWebAppSnapshot** zwraca wszystkie migawki dla aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="23aed-108">The **Get-AzWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="23aed-109">Migawki to automatyczne tworzenie kopii zapasowych plików i ustawień aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="23aed-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="23aed-110">Migawkę można przywrócić przy użyciu polecenia cmdlet **Restore-AzWebAppSnapshot** .</span><span class="sxs-lookup"><span data-stu-id="23aed-110">A snapshot can be restored with the **Restore-AzWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="23aed-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="23aed-111">EXAMPLES</span></span>

### <span data-ttu-id="23aed-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="23aed-112">Example 1</span></span>
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="23aed-113">Pobierz migawki dla aplikacji sieci Web o nazwie "ContosoApp" z miejscem o nazwie "przemieszczanie" w grupie zasobów "Default-Web-Zachodnia"</span><span class="sxs-lookup"><span data-stu-id="23aed-113">Get the snapshots for a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="23aed-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="23aed-114">PARAMETERS</span></span>

### <span data-ttu-id="23aed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23aed-115">-DefaultProfile</span></span>
<span data-ttu-id="23aed-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="23aed-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23aed-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="23aed-117">-Name</span></span>
<span data-ttu-id="23aed-118">Nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="23aed-118">The name of the web app.</span></span>

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

### <span data-ttu-id="23aed-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23aed-119">-ResourceGroupName</span></span>
<span data-ttu-id="23aed-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="23aed-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="23aed-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="23aed-121">-Slot</span></span>
<span data-ttu-id="23aed-122">Nazwa miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="23aed-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="23aed-123">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="23aed-123">-UseDisasterRecovery</span></span>
<span data-ttu-id="23aed-124">Odczytaj migawki z pomocniczej jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="23aed-124">Read the snapshots from a secondary scale unit.</span></span>

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

### <span data-ttu-id="23aed-125">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="23aed-125">-WebApp</span></span>
<span data-ttu-id="23aed-126">Obiekt aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="23aed-126">The web app object</span></span>

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

### <span data-ttu-id="23aed-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23aed-127">CommonParameters</span></span>
<span data-ttu-id="23aed-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23aed-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23aed-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23aed-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23aed-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23aed-130">INPUTS</span></span>

### <span data-ttu-id="23aed-131">System. String</span><span class="sxs-lookup"><span data-stu-id="23aed-131">System.String</span></span>

### <span data-ttu-id="23aed-132">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="23aed-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="23aed-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="23aed-133">OUTPUTS</span></span>

### <span data-ttu-id="23aed-134">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="23aed-134">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="23aed-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="23aed-135">NOTES</span></span>

## <span data-ttu-id="23aed-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23aed-136">RELATED LINKS</span></span>
