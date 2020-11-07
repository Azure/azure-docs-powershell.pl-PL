---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappsnapshot
schema: 2.0.0
ms.openlocfilehash: 754ff798ca001e2c6b5a067f6e6244704fc2f617
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897526"
---
# <span data-ttu-id="c3829-101">Get-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="c3829-101">Get-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="c3829-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c3829-102">SYNOPSIS</span></span>
<span data-ttu-id="c3829-103">Pobiera migawki dostępne dla aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="c3829-103">Gets the snapshots available for a web app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3829-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c3829-104">SYNTAX</span></span>

### <span data-ttu-id="c3829-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="c3829-105">FromResourceName</span></span>
```
Get-AzureRmWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="c3829-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="c3829-106">FromWebApp</span></span>
```
Get-AzureRmWebAppSnapshot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="c3829-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c3829-107">DESCRIPTION</span></span>
<span data-ttu-id="c3829-108">Polecenie cmdlet **Get-AzureRmWebAppSnapshot** zwraca wszystkie migawki dla aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="c3829-108">The **Get-AzureRmWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="c3829-109">Migawki to automatyczne tworzenie kopii zapasowych plików i ustawień aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="c3829-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="c3829-110">Migawkę można przywrócić przy użyciu polecenia cmdlet **Restore-AzureRmWebAppSnapshot** .</span><span class="sxs-lookup"><span data-stu-id="c3829-110">A snapshot can be restored with the **Restore-AzureRmWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="c3829-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c3829-111">EXAMPLES</span></span>

### <span data-ttu-id="c3829-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c3829-112">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="c3829-113">Pobierz migawki dla aplikacji sieci Web o nazwie "ConstosoApp" z miejscem o nazwie "przemieszczanie" w grupie zasobów "Default-Web-Zachodnia"</span><span class="sxs-lookup"><span data-stu-id="c3829-113">Get the snapshots for a web app named "ConstosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="c3829-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c3829-114">PARAMETERS</span></span>

### <span data-ttu-id="c3829-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3829-115">-DefaultProfile</span></span>
<span data-ttu-id="c3829-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c3829-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3829-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c3829-117">-Name</span></span>
<span data-ttu-id="c3829-118">Nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="c3829-118">The name of the web app.</span></span>

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

### <span data-ttu-id="c3829-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3829-119">-ResourceGroupName</span></span>
<span data-ttu-id="c3829-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c3829-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="c3829-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="c3829-121">-Slot</span></span>
<span data-ttu-id="c3829-122">Nazwa miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="c3829-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="c3829-123">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="c3829-123">-WebApp</span></span>
<span data-ttu-id="c3829-124">Obiekt aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="c3829-124">The web app object</span></span>

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

## <span data-ttu-id="c3829-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3829-125">INPUTS</span></span>

### <span data-ttu-id="c3829-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c3829-126">System.String</span></span>
<span data-ttu-id="c3829-127">Microsoft. Azure. Management. Web. models. site</span><span class="sxs-lookup"><span data-stu-id="c3829-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>


## <span data-ttu-id="c3829-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c3829-128">OUTPUTS</span></span>

### <span data-ttu-id="c3829-129">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="c3829-129">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>


## <span data-ttu-id="c3829-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c3829-130">NOTES</span></span>

## <span data-ttu-id="c3829-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3829-131">RELATED LINKS</span></span>

