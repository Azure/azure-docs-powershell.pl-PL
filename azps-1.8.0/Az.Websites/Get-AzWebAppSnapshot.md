---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: fab46f997492c366857c7d13bea38543cca4e91c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707309"
---
# <span data-ttu-id="1ac85-101">Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="1ac85-101">Get-AzWebAppSnapshot</span></span>

## <span data-ttu-id="1ac85-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1ac85-102">SYNOPSIS</span></span>
<span data-ttu-id="1ac85-103">Pobiera migawki dostępne dla aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="1ac85-103">Gets the snapshots available for a web app.</span></span>

## <span data-ttu-id="1ac85-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1ac85-104">SYNTAX</span></span>

### <span data-ttu-id="1ac85-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="1ac85-105">FromResourceName</span></span>
```
Get-AzWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ac85-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="1ac85-106">FromWebApp</span></span>
```
Get-AzWebAppSnapshot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ac85-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1ac85-107">DESCRIPTION</span></span>
<span data-ttu-id="1ac85-108">Polecenie cmdlet **Get-AzWebAppSnapshot** zwraca wszystkie migawki dla aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="1ac85-108">The **Get-AzWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="1ac85-109">Migawki to automatyczne tworzenie kopii zapasowych plików i ustawień aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="1ac85-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="1ac85-110">Migawkę można przywrócić przy użyciu polecenia cmdlet **Restore-AzWebAppSnapshot** .</span><span class="sxs-lookup"><span data-stu-id="1ac85-110">A snapshot can be restored with the **Restore-AzWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="1ac85-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1ac85-111">EXAMPLES</span></span>

### <span data-ttu-id="1ac85-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1ac85-112">Example 1</span></span>
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="1ac85-113">Pobierz migawki dla aplikacji sieci Web o nazwie "ConstosoApp" z miejscem o nazwie "przemieszczanie" w grupie zasobów "Default-Web-Zachodnia"</span><span class="sxs-lookup"><span data-stu-id="1ac85-113">Get the snapshots for a web app named "ConstosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="1ac85-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1ac85-114">PARAMETERS</span></span>

### <span data-ttu-id="1ac85-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ac85-115">-DefaultProfile</span></span>
<span data-ttu-id="1ac85-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1ac85-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ac85-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1ac85-117">-Name</span></span>
<span data-ttu-id="1ac85-118">Nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="1ac85-118">The name of the web app.</span></span>

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

### <span data-ttu-id="1ac85-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ac85-119">-ResourceGroupName</span></span>
<span data-ttu-id="1ac85-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1ac85-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="1ac85-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="1ac85-121">-Slot</span></span>
<span data-ttu-id="1ac85-122">Nazwa miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="1ac85-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="1ac85-123">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="1ac85-123">-WebApp</span></span>
<span data-ttu-id="1ac85-124">Obiekt aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="1ac85-124">The web app object</span></span>

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

### <span data-ttu-id="1ac85-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ac85-125">CommonParameters</span></span>
<span data-ttu-id="1ac85-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ac85-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ac85-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ac85-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ac85-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ac85-128">INPUTS</span></span>

### <span data-ttu-id="1ac85-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1ac85-129">System.String</span></span>

### <span data-ttu-id="1ac85-130">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="1ac85-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1ac85-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1ac85-131">OUTPUTS</span></span>

### <span data-ttu-id="1ac85-132">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="1ac85-132">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="1ac85-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1ac85-133">NOTES</span></span>

## <span data-ttu-id="1ac85-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ac85-134">RELATED LINKS</span></span>
