---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappbackup
schema: 2.0.0
ms.openlocfilehash: ad27e4f9f7e042fa5a649fb06131167f38f1a1be
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899022"
---
# <span data-ttu-id="f4a78-101">Remove-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="f4a78-101">Remove-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="f4a78-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f4a78-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4a78-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f4a78-103">SYNTAX</span></span>

### <span data-ttu-id="f4a78-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="f4a78-104">FromResourceName</span></span>
```
Remove-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4a78-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="f4a78-105">FromWebApp</span></span>
```
Remove-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4a78-106">Opis</span><span class="sxs-lookup"><span data-stu-id="f4a78-106">DESCRIPTION</span></span>
<span data-ttu-id="f4a78-107">Polecenie cmdlet **Remove-AzureRmWebAppBackup** usuwa określoną kopię zapasową aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="f4a78-107">The **Remove-AzureRmWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="f4a78-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f4a78-108">EXAMPLES</span></span>

### <span data-ttu-id="f4a78-109">1:1</span><span class="sxs-lookup"><span data-stu-id="f4a78-109">1:</span></span>
```
PS C:\>Remove-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="f4a78-110">To polecenie usuwa kopię zapasową z IDENTYFIKATORem "12345" z aplikacji sieci Web o nazwie WebAppStandard należącej do grupy zasobów Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="f4a78-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="f4a78-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f4a78-111">PARAMETERS</span></span>

### <span data-ttu-id="f4a78-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="f4a78-112">-BackupId</span></span>
<span data-ttu-id="f4a78-113">Identyfikator kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="f4a78-113">Backup Id</span></span>

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

### <span data-ttu-id="f4a78-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4a78-114">-DefaultProfile</span></span>
<span data-ttu-id="f4a78-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f4a78-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4a78-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f4a78-116">-Name</span></span>
<span data-ttu-id="f4a78-117">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="f4a78-117">WebApp Name</span></span>

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

### <span data-ttu-id="f4a78-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4a78-118">-ResourceGroupName</span></span>
<span data-ttu-id="f4a78-119">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f4a78-119">Resource Group Name</span></span>

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

### <span data-ttu-id="f4a78-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="f4a78-120">-Slot</span></span>
<span data-ttu-id="f4a78-121">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="f4a78-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="f4a78-122">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="f4a78-122">-WebApp</span></span>
<span data-ttu-id="f4a78-123">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="f4a78-123">WebApp Object</span></span>

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

### <span data-ttu-id="f4a78-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4a78-124">CommonParameters</span></span>
<span data-ttu-id="f4a78-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4a78-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4a78-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4a78-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4a78-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4a78-127">INPUTS</span></span>

### <span data-ttu-id="f4a78-128">Klienta</span><span class="sxs-lookup"><span data-stu-id="f4a78-128">Site</span></span>
<span data-ttu-id="f4a78-129">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="f4a78-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f4a78-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f4a78-130">OUTPUTS</span></span>

### <span data-ttu-id="f4a78-131">Microsoft. Azure. Management. Web. MODELES. BackupItem</span><span class="sxs-lookup"><span data-stu-id="f4a78-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="f4a78-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f4a78-132">NOTES</span></span>

## <span data-ttu-id="f4a78-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f4a78-133">RELATED LINKS</span></span>

