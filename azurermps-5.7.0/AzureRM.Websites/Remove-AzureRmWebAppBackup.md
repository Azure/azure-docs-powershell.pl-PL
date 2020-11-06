---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppBackup.md
ms.openlocfilehash: f2b6e4b4ea09605a55e179e682065de70ef92024
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542172"
---
# <span data-ttu-id="dd3c3-101">Remove-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="dd3c3-101">Remove-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="dd3c3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dd3c3-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd3c3-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dd3c3-103">SYNTAX</span></span>

### <span data-ttu-id="dd3c3-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="dd3c3-104">FromResourceName</span></span>
```
Remove-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd3c3-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="dd3c3-105">FromWebApp</span></span>
```
Remove-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd3c3-106">Opis</span><span class="sxs-lookup"><span data-stu-id="dd3c3-106">DESCRIPTION</span></span>
<span data-ttu-id="dd3c3-107">Polecenie cmdlet **Remove-AzureRmWebAppBackup** usuwa określoną kopię zapasową aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="dd3c3-107">The **Remove-AzureRmWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="dd3c3-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dd3c3-108">EXAMPLES</span></span>

### <span data-ttu-id="dd3c3-109">1:1</span><span class="sxs-lookup"><span data-stu-id="dd3c3-109">1:</span></span>
```
PS C:\>Remove-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="dd3c3-110">To polecenie usuwa kopię zapasową z IDENTYFIKATORem "12345" z aplikacji sieci Web o nazwie WebAppStandard należącej do grupy zasobów Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="dd3c3-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="dd3c3-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dd3c3-111">PARAMETERS</span></span>

### <span data-ttu-id="dd3c3-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="dd3c3-112">-BackupId</span></span>
<span data-ttu-id="dd3c3-113">Identyfikator kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="dd3c3-113">Backup Id</span></span>

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

### <span data-ttu-id="dd3c3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd3c3-114">-DefaultProfile</span></span>
<span data-ttu-id="dd3c3-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dd3c3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd3c3-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dd3c3-116">-Name</span></span>
<span data-ttu-id="dd3c3-117">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="dd3c3-117">WebApp Name</span></span>

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

### <span data-ttu-id="dd3c3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd3c3-118">-ResourceGroupName</span></span>
<span data-ttu-id="dd3c3-119">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="dd3c3-119">Resource Group Name</span></span>

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

### <span data-ttu-id="dd3c3-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="dd3c3-120">-Slot</span></span>
<span data-ttu-id="dd3c3-121">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="dd3c3-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="dd3c3-122">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="dd3c3-122">-WebApp</span></span>
<span data-ttu-id="dd3c3-123">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="dd3c3-123">WebApp Object</span></span>

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

### <span data-ttu-id="dd3c3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd3c3-124">CommonParameters</span></span>
<span data-ttu-id="dd3c3-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd3c3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd3c3-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd3c3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd3c3-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd3c3-127">INPUTS</span></span>

### <span data-ttu-id="dd3c3-128">Klienta</span><span class="sxs-lookup"><span data-stu-id="dd3c3-128">Site</span></span>
<span data-ttu-id="dd3c3-129">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="dd3c3-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="dd3c3-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dd3c3-130">OUTPUTS</span></span>

### <span data-ttu-id="dd3c3-131">Microsoft. Azure. Management. Web. MODELES. BackupItem</span><span class="sxs-lookup"><span data-stu-id="dd3c3-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="dd3c3-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dd3c3-132">NOTES</span></span>

## <span data-ttu-id="dd3c3-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd3c3-133">RELATED LINKS</span></span>

