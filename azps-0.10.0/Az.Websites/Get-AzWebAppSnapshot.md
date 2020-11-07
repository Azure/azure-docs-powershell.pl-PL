---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: 1374bfb67b3150b2c65841d91fd440a83f791b95
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891922"
---
# <span data-ttu-id="958ab-101">Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="958ab-101">Get-AzWebAppSnapshot</span></span>

## <span data-ttu-id="958ab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="958ab-102">SYNOPSIS</span></span>
<span data-ttu-id="958ab-103">Pobiera migawki dostępne dla aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="958ab-103">Gets the snapshots available for a web app.</span></span>

## <span data-ttu-id="958ab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="958ab-104">SYNTAX</span></span>

### <span data-ttu-id="958ab-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="958ab-105">FromResourceName</span></span>
```
Get-AzWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="958ab-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="958ab-106">FromWebApp</span></span>
```
Get-AzWebAppSnapshot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="958ab-107">Opis</span><span class="sxs-lookup"><span data-stu-id="958ab-107">DESCRIPTION</span></span>
<span data-ttu-id="958ab-108">Polecenie cmdlet **Get-AzWebAppSnapshot** zwraca wszystkie migawki dla aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="958ab-108">The **Get-AzWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="958ab-109">Migawki to automatyczne tworzenie kopii zapasowych plików i ustawień aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="958ab-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="958ab-110">Migawkę można przywrócić przy użyciu polecenia cmdlet **Restore-AzWebAppSnapshot** .</span><span class="sxs-lookup"><span data-stu-id="958ab-110">A snapshot can be restored with the **Restore-AzWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="958ab-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="958ab-111">EXAMPLES</span></span>

### <span data-ttu-id="958ab-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="958ab-112">Example 1</span></span>
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="958ab-113">Pobierz migawki dla aplikacji sieci Web o nazwie "ConstosoApp" z miejscem o nazwie "przemieszczanie" w grupie zasobów "Default-Web-Zachodnia"</span><span class="sxs-lookup"><span data-stu-id="958ab-113">Get the snapshots for a web app named "ConstosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="958ab-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="958ab-114">PARAMETERS</span></span>

### <span data-ttu-id="958ab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="958ab-115">-DefaultProfile</span></span>
<span data-ttu-id="958ab-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="958ab-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="958ab-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="958ab-117">-Name</span></span>
<span data-ttu-id="958ab-118">Nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="958ab-118">The name of the web app.</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="958ab-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="958ab-119">-ResourceGroupName</span></span>
<span data-ttu-id="958ab-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="958ab-120">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="958ab-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="958ab-121">-Slot</span></span>
<span data-ttu-id="958ab-122">Nazwa miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="958ab-122">The name of the web app slot.</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="958ab-123">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="958ab-123">-WebApp</span></span>
<span data-ttu-id="958ab-124">Obiekt aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="958ab-124">The web app object</span></span>

```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

## <span data-ttu-id="958ab-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="958ab-125">INPUTS</span></span>

### <span data-ttu-id="958ab-126">System. String</span><span class="sxs-lookup"><span data-stu-id="958ab-126">System.String</span></span>
<span data-ttu-id="958ab-127">Microsoft. Azure. Management. Web. models. site</span><span class="sxs-lookup"><span data-stu-id="958ab-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>


## <span data-ttu-id="958ab-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="958ab-128">OUTPUTS</span></span>

### <span data-ttu-id="958ab-129">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="958ab-129">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>


## <span data-ttu-id="958ab-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="958ab-130">NOTES</span></span>

## <span data-ttu-id="958ab-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="958ab-131">RELATED LINKS</span></span>

