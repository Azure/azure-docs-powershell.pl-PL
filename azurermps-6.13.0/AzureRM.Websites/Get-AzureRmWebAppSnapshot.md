---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSnapshot.md
ms.openlocfilehash: 292364ae6355c640ed66116c84289fe303acdd53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524206"
---
# <span data-ttu-id="a52cb-101">Get-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="a52cb-101">Get-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="a52cb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a52cb-102">SYNOPSIS</span></span>
<span data-ttu-id="a52cb-103">Pobiera migawki dostępne dla aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="a52cb-103">Gets the snapshots available for a web app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a52cb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a52cb-104">SYNTAX</span></span>

### <span data-ttu-id="a52cb-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="a52cb-105">FromResourceName</span></span>
```
Get-AzureRmWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a52cb-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="a52cb-106">FromWebApp</span></span>
```
Get-AzureRmWebAppSnapshot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a52cb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a52cb-107">DESCRIPTION</span></span>
<span data-ttu-id="a52cb-108">Polecenie cmdlet **Get-AzureRmWebAppSnapshot** zwraca wszystkie migawki dla aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="a52cb-108">The **Get-AzureRmWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="a52cb-109">Migawki to automatyczne tworzenie kopii zapasowych plików i ustawień aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="a52cb-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="a52cb-110">Migawkę można przywrócić przy użyciu polecenia cmdlet **Restore-AzureRmWebAppSnapshot** .</span><span class="sxs-lookup"><span data-stu-id="a52cb-110">A snapshot can be restored with the **Restore-AzureRmWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="a52cb-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a52cb-111">EXAMPLES</span></span>

### <span data-ttu-id="a52cb-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a52cb-112">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="a52cb-113">Pobierz migawki dla aplikacji sieci Web o nazwie "ConstosoApp" z miejscem o nazwie "przemieszczanie" w grupie zasobów "Default-Web-Zachodnia"</span><span class="sxs-lookup"><span data-stu-id="a52cb-113">Get the snapshots for a web app named "ConstosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="a52cb-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a52cb-114">PARAMETERS</span></span>

### <span data-ttu-id="a52cb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a52cb-115">-DefaultProfile</span></span>
<span data-ttu-id="a52cb-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a52cb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a52cb-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a52cb-117">-Name</span></span>
<span data-ttu-id="a52cb-118">Nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="a52cb-118">The name of the web app.</span></span>

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

### <span data-ttu-id="a52cb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a52cb-119">-ResourceGroupName</span></span>
<span data-ttu-id="a52cb-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a52cb-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="a52cb-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="a52cb-121">-Slot</span></span>
<span data-ttu-id="a52cb-122">Nazwa miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="a52cb-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="a52cb-123">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="a52cb-123">-WebApp</span></span>
<span data-ttu-id="a52cb-124">Obiekt aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="a52cb-124">The web app object</span></span>

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

### <span data-ttu-id="a52cb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a52cb-125">CommonParameters</span></span>
<span data-ttu-id="a52cb-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a52cb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a52cb-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a52cb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a52cb-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a52cb-128">INPUTS</span></span>

### <span data-ttu-id="a52cb-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a52cb-129">System.String</span></span>

### <span data-ttu-id="a52cb-130">Microsoft. Azure. Management. Web. models. site</span><span class="sxs-lookup"><span data-stu-id="a52cb-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="a52cb-131">Parametry: aplikacji (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a52cb-131">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="a52cb-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a52cb-132">OUTPUTS</span></span>

### <span data-ttu-id="a52cb-133">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="a52cb-133">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="a52cb-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a52cb-134">NOTES</span></span>

## <span data-ttu-id="a52cb-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a52cb-135">RELATED LINKS</span></span>
