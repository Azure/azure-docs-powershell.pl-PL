---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 4c6dc810d35feedd0d0d43e0bd3b3efb7c9b6641
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891946"
---
# <span data-ttu-id="6028c-101">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="6028c-101">Get-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="6028c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6028c-102">SYNOPSIS</span></span>

## <span data-ttu-id="6028c-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6028c-103">SYNTAX</span></span>

### <span data-ttu-id="6028c-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="6028c-104">FromResourceName</span></span>
```
Get-AzWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6028c-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="6028c-105">FromWebApp</span></span>
```
Get-AzWebAppBackupConfiguration [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6028c-106">Opis</span><span class="sxs-lookup"><span data-stu-id="6028c-106">DESCRIPTION</span></span>
<span data-ttu-id="6028c-107">Polecenie cmdlet **Get-AzWebAppBackupConfiguration** Pobiera konfigurację kopii zapasowej aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="6028c-107">The **Get-AzWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="6028c-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6028c-108">EXAMPLES</span></span>

### <span data-ttu-id="6028c-109">1:1</span><span class="sxs-lookup"><span data-stu-id="6028c-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="6028c-110">To polecenie pobiera konfigurację kopii zapasowej z aplikacji sieci Web o nazwie WebAppStandard należącej do grupy zasobów Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="6028c-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="6028c-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6028c-111">PARAMETERS</span></span>

### <span data-ttu-id="6028c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6028c-112">-DefaultProfile</span></span>
<span data-ttu-id="6028c-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6028c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6028c-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6028c-114">-Name</span></span>
<span data-ttu-id="6028c-115">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="6028c-115">WebApp Name</span></span>

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

### <span data-ttu-id="6028c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6028c-116">-ResourceGroupName</span></span>
<span data-ttu-id="6028c-117">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6028c-117">Resource Group Name</span></span>

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

### <span data-ttu-id="6028c-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="6028c-118">-Slot</span></span>
<span data-ttu-id="6028c-119">Nazwa gniazda</span><span class="sxs-lookup"><span data-stu-id="6028c-119">Slot Name</span></span>

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

### <span data-ttu-id="6028c-120">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="6028c-120">-WebApp</span></span>
<span data-ttu-id="6028c-121">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="6028c-121">WebApp Name</span></span>

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

### <span data-ttu-id="6028c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6028c-122">CommonParameters</span></span>
<span data-ttu-id="6028c-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6028c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6028c-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6028c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6028c-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6028c-125">INPUTS</span></span>

### <span data-ttu-id="6028c-126">Klienta</span><span class="sxs-lookup"><span data-stu-id="6028c-126">Site</span></span>
<span data-ttu-id="6028c-127">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="6028c-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="6028c-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6028c-128">OUTPUTS</span></span>

### <span data-ttu-id="6028c-129">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="6028c-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="6028c-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6028c-130">NOTES</span></span>

## <span data-ttu-id="6028c-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6028c-131">RELATED LINKS</span></span>

