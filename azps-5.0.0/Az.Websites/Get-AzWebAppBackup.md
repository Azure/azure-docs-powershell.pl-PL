---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
ms.openlocfilehash: e8c3f7543062613527e7f52be2cd6493f53c5f60
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308652"
---
# <span data-ttu-id="b8f67-101">Get-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="b8f67-101">Get-AzWebAppBackup</span></span>

## <span data-ttu-id="b8f67-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b8f67-102">SYNOPSIS</span></span>

## <span data-ttu-id="b8f67-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b8f67-103">SYNTAX</span></span>

### <span data-ttu-id="b8f67-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="b8f67-104">FromResourceName</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8f67-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="b8f67-105">FromWebApp</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8f67-106">Opis</span><span class="sxs-lookup"><span data-stu-id="b8f67-106">DESCRIPTION</span></span>
<span data-ttu-id="b8f67-107">Polecenie cmdlet **Get-AzWebAppBackup** pobiera określoną kopię zapasową aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="b8f67-107">The **Get-AzWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="b8f67-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b8f67-108">EXAMPLES</span></span>

### <span data-ttu-id="b8f67-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b8f67-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="b8f67-110">To polecenie pobiera kopię zapasową o IDENTYFIKATORze "12345" z aplikacji sieci Web o nazwie WebAppStandard należącej do grupy zasobów Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="b8f67-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="b8f67-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b8f67-111">PARAMETERS</span></span>

### <span data-ttu-id="b8f67-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="b8f67-112">-BackupId</span></span>
<span data-ttu-id="b8f67-113">Identyfikator kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="b8f67-113">Backup Id</span></span>

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

### <span data-ttu-id="b8f67-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8f67-114">-DefaultProfile</span></span>
<span data-ttu-id="b8f67-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b8f67-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8f67-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b8f67-116">-Name</span></span>
<span data-ttu-id="b8f67-117">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="b8f67-117">Webapp Name</span></span>

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

### <span data-ttu-id="b8f67-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8f67-118">-ResourceGroupName</span></span>
<span data-ttu-id="b8f67-119">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b8f67-119">Resource Group Name</span></span>

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

### <span data-ttu-id="b8f67-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="b8f67-120">-Slot</span></span>
<span data-ttu-id="b8f67-121">Nazwa gniazda</span><span class="sxs-lookup"><span data-stu-id="b8f67-121">Slot Name</span></span>

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

### <span data-ttu-id="b8f67-122">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="b8f67-122">-WebApp</span></span>
<span data-ttu-id="b8f67-123">Potok aplikacji</span><span class="sxs-lookup"><span data-stu-id="b8f67-123">Piped WebApp</span></span>

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

### <span data-ttu-id="b8f67-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8f67-124">CommonParameters</span></span>
<span data-ttu-id="b8f67-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8f67-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8f67-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8f67-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8f67-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8f67-127">INPUTS</span></span>

### <span data-ttu-id="b8f67-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b8f67-128">System.String</span></span>

### <span data-ttu-id="b8f67-129">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="b8f67-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b8f67-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b8f67-130">OUTPUTS</span></span>

### <span data-ttu-id="b8f67-131">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="b8f67-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="b8f67-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b8f67-132">NOTES</span></span>

## <span data-ttu-id="b8f67-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b8f67-133">RELATED LINKS</span></span>
