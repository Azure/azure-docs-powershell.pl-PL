---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
ms.openlocfilehash: 65748ed269a7cb42914c98549c68be32812f71f3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894917"
---
# <span data-ttu-id="c5117-101">Get-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="c5117-101">Get-AzWebAppBackup</span></span>

## <span data-ttu-id="c5117-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c5117-102">SYNOPSIS</span></span>

## <span data-ttu-id="c5117-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c5117-103">SYNTAX</span></span>

### <span data-ttu-id="c5117-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="c5117-104">FromResourceName</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5117-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="c5117-105">FromWebApp</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c5117-106">Opis</span><span class="sxs-lookup"><span data-stu-id="c5117-106">DESCRIPTION</span></span>
<span data-ttu-id="c5117-107">Polecenie cmdlet **Get-AzWebAppBackup** pobiera określoną kopię zapasową aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c5117-107">The **Get-AzWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="c5117-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c5117-108">EXAMPLES</span></span>

### <span data-ttu-id="c5117-109">1:1</span><span class="sxs-lookup"><span data-stu-id="c5117-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="c5117-110">To polecenie pobiera kopię zapasową o IDENTYFIKATORze "12345" z aplikacji sieci Web o nazwie WebAppStandard należącej do grupy zasobów Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="c5117-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="c5117-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c5117-111">PARAMETERS</span></span>

### <span data-ttu-id="c5117-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="c5117-112">-BackupId</span></span>
<span data-ttu-id="c5117-113">Identyfikator kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="c5117-113">Backup Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5117-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5117-114">-DefaultProfile</span></span>
<span data-ttu-id="c5117-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c5117-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5117-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c5117-116">-Name</span></span>
<span data-ttu-id="c5117-117">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="c5117-117">Webapp Name</span></span>

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

### <span data-ttu-id="c5117-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5117-118">-ResourceGroupName</span></span>
<span data-ttu-id="c5117-119">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c5117-119">Resource Group Name</span></span>

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

### <span data-ttu-id="c5117-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="c5117-120">-Slot</span></span>
<span data-ttu-id="c5117-121">Nazwa gniazda</span><span class="sxs-lookup"><span data-stu-id="c5117-121">Slot Name</span></span>

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

### <span data-ttu-id="c5117-122">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="c5117-122">-WebApp</span></span>
<span data-ttu-id="c5117-123">Potok aplikacji</span><span class="sxs-lookup"><span data-stu-id="c5117-123">Piped WebApp</span></span>

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

### <span data-ttu-id="c5117-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5117-124">CommonParameters</span></span>
<span data-ttu-id="c5117-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5117-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5117-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5117-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5117-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c5117-127">INPUTS</span></span>

### <span data-ttu-id="c5117-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c5117-128">System.String</span></span>

### <span data-ttu-id="c5117-129">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="c5117-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c5117-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c5117-130">OUTPUTS</span></span>

### <span data-ttu-id="c5117-131">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="c5117-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="c5117-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c5117-132">NOTES</span></span>

## <span data-ttu-id="c5117-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c5117-133">RELATED LINKS</span></span>
