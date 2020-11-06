---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackup.md
ms.openlocfilehash: 87ecbd0c18d90a06b986ddbe4fd00e23d28b836c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550443"
---
# <span data-ttu-id="a31d2-101">Get-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="a31d2-101">Get-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="a31d2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a31d2-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a31d2-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a31d2-103">SYNTAX</span></span>

### <span data-ttu-id="a31d2-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="a31d2-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a31d2-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="a31d2-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a31d2-106">Opis</span><span class="sxs-lookup"><span data-stu-id="a31d2-106">DESCRIPTION</span></span>
<span data-ttu-id="a31d2-107">Polecenie cmdlet **Get-AzureRmWebAppBackup** pobiera określoną kopię zapasową aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="a31d2-107">The **Get-AzureRmWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="a31d2-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a31d2-108">EXAMPLES</span></span>

### <span data-ttu-id="a31d2-109">1:1</span><span class="sxs-lookup"><span data-stu-id="a31d2-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="a31d2-110">To polecenie pobiera kopię zapasową o IDENTYFIKATORze "12345" z aplikacji sieci Web o nazwie WebAppStandard należącej do grupy zasobów Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="a31d2-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="a31d2-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a31d2-111">PARAMETERS</span></span>

### <span data-ttu-id="a31d2-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="a31d2-112">-BackupId</span></span>
<span data-ttu-id="a31d2-113">Identyfikator kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="a31d2-113">Backup Id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a31d2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a31d2-114">-DefaultProfile</span></span>
<span data-ttu-id="a31d2-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a31d2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a31d2-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a31d2-116">-Name</span></span>
<span data-ttu-id="a31d2-117">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="a31d2-117">Webapp Name</span></span>

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

### <span data-ttu-id="a31d2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a31d2-118">-ResourceGroupName</span></span>
<span data-ttu-id="a31d2-119">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a31d2-119">Resource Group Name</span></span>

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

### <span data-ttu-id="a31d2-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="a31d2-120">-Slot</span></span>
<span data-ttu-id="a31d2-121">Nazwa gniazda</span><span class="sxs-lookup"><span data-stu-id="a31d2-121">Slot Name</span></span>

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

### <span data-ttu-id="a31d2-122">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="a31d2-122">-WebApp</span></span>
<span data-ttu-id="a31d2-123">Potok aplikacji</span><span class="sxs-lookup"><span data-stu-id="a31d2-123">Piped WebApp</span></span>

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

### <span data-ttu-id="a31d2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a31d2-124">CommonParameters</span></span>
<span data-ttu-id="a31d2-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a31d2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a31d2-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a31d2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a31d2-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a31d2-127">INPUTS</span></span>

### <span data-ttu-id="a31d2-128">Klienta</span><span class="sxs-lookup"><span data-stu-id="a31d2-128">Site</span></span>
<span data-ttu-id="a31d2-129">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="a31d2-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="a31d2-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a31d2-130">OUTPUTS</span></span>

### <span data-ttu-id="a31d2-131">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="a31d2-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="a31d2-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a31d2-132">NOTES</span></span>

## <span data-ttu-id="a31d2-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a31d2-133">RELATED LINKS</span></span>

