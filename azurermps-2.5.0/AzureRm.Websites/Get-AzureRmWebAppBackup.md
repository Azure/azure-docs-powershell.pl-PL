---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackup
schema: 2.0.0
ms.openlocfilehash: c6d5809211910987e06cff024d7510a70ad71a4e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897210"
---
# <span data-ttu-id="e1d7d-101">Get-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="e1d7d-101">Get-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="e1d7d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e1d7d-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1d7d-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e1d7d-103">SYNTAX</span></span>

### <span data-ttu-id="e1d7d-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="e1d7d-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1d7d-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="e1d7d-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1d7d-106">Opis</span><span class="sxs-lookup"><span data-stu-id="e1d7d-106">DESCRIPTION</span></span>
<span data-ttu-id="e1d7d-107">Polecenie cmdlet **Get-AzureRmWebAppBackup** pobiera określoną kopię zapasową aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="e1d7d-107">The **Get-AzureRmWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="e1d7d-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e1d7d-108">EXAMPLES</span></span>

### <span data-ttu-id="e1d7d-109">1:1</span><span class="sxs-lookup"><span data-stu-id="e1d7d-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="e1d7d-110">To polecenie pobiera kopię zapasową o IDENTYFIKATORze "12345" z aplikacji sieci Web o nazwie WebAppStandard należącej do grupy zasobów Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="e1d7d-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="e1d7d-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e1d7d-111">PARAMETERS</span></span>

### <span data-ttu-id="e1d7d-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="e1d7d-112">-BackupId</span></span>
<span data-ttu-id="e1d7d-113">Identyfikator kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="e1d7d-113">Backup Id</span></span>

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

### <span data-ttu-id="e1d7d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1d7d-114">-DefaultProfile</span></span>
<span data-ttu-id="e1d7d-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e1d7d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1d7d-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e1d7d-116">-Name</span></span>
<span data-ttu-id="e1d7d-117">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="e1d7d-117">Webapp Name</span></span>

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

### <span data-ttu-id="e1d7d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1d7d-118">-ResourceGroupName</span></span>
<span data-ttu-id="e1d7d-119">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e1d7d-119">Resource Group Name</span></span>

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

### <span data-ttu-id="e1d7d-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="e1d7d-120">-Slot</span></span>
<span data-ttu-id="e1d7d-121">Nazwa gniazda</span><span class="sxs-lookup"><span data-stu-id="e1d7d-121">Slot Name</span></span>

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

### <span data-ttu-id="e1d7d-122">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="e1d7d-122">-WebApp</span></span>
<span data-ttu-id="e1d7d-123">Potok aplikacji</span><span class="sxs-lookup"><span data-stu-id="e1d7d-123">Piped WebApp</span></span>

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

### <span data-ttu-id="e1d7d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1d7d-124">CommonParameters</span></span>
<span data-ttu-id="e1d7d-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1d7d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1d7d-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1d7d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1d7d-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1d7d-127">INPUTS</span></span>

### <span data-ttu-id="e1d7d-128">Klienta</span><span class="sxs-lookup"><span data-stu-id="e1d7d-128">Site</span></span>
<span data-ttu-id="e1d7d-129">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="e1d7d-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="e1d7d-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e1d7d-130">OUTPUTS</span></span>

### <span data-ttu-id="e1d7d-131">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="e1d7d-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="e1d7d-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e1d7d-132">NOTES</span></span>

## <span data-ttu-id="e1d7d-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1d7d-133">RELATED LINKS</span></span>

