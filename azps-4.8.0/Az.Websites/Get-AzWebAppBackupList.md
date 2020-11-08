---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
ms.openlocfilehash: 6ea805f1e3a3711c2efe6faefd73edf06c4b51fd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220975"
---
# <span data-ttu-id="e1bcc-101">Get-AzWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="e1bcc-101">Get-AzWebAppBackupList</span></span>

## <span data-ttu-id="e1bcc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e1bcc-102">SYNOPSIS</span></span>

## <span data-ttu-id="e1bcc-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e1bcc-103">SYNTAX</span></span>

### <span data-ttu-id="e1bcc-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="e1bcc-104">FromResourceName</span></span>
```
Get-AzWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1bcc-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="e1bcc-105">FromWebApp</span></span>
```
Get-AzWebAppBackupList [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1bcc-106">Opis</span><span class="sxs-lookup"><span data-stu-id="e1bcc-106">DESCRIPTION</span></span>
<span data-ttu-id="e1bcc-107">Polecenie cmdlet **Get-AzWebAppBackupList** pobiera listę kopii zapasowych aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="e1bcc-107">The **Get-AzWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="e1bcc-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e1bcc-108">EXAMPLES</span></span>

### <span data-ttu-id="e1bcc-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e1bcc-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="e1bcc-110">To polecenie zwraca listę kopii zapasowych odnoszącą się do aplikacji WebAppStandard skojarzonych z ContosoResourceGroup grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="e1bcc-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="e1bcc-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e1bcc-111">PARAMETERS</span></span>

### <span data-ttu-id="e1bcc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1bcc-112">-DefaultProfile</span></span>
<span data-ttu-id="e1bcc-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e1bcc-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1bcc-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e1bcc-114">-Name</span></span>
<span data-ttu-id="e1bcc-115">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="e1bcc-115">WebApp Name</span></span>

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

### <span data-ttu-id="e1bcc-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1bcc-116">-ResourceGroupName</span></span>
<span data-ttu-id="e1bcc-117">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e1bcc-117">Resource Group Name</span></span>

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

### <span data-ttu-id="e1bcc-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="e1bcc-118">-Slot</span></span>
<span data-ttu-id="e1bcc-119">Nazwa gniazda</span><span class="sxs-lookup"><span data-stu-id="e1bcc-119">Slot name</span></span>

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

### <span data-ttu-id="e1bcc-120">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="e1bcc-120">-WebApp</span></span>
<span data-ttu-id="e1bcc-121">Potok aplikacji</span><span class="sxs-lookup"><span data-stu-id="e1bcc-121">Piped WebApp</span></span>

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

### <span data-ttu-id="e1bcc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1bcc-122">CommonParameters</span></span>
<span data-ttu-id="e1bcc-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1bcc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1bcc-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1bcc-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1bcc-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1bcc-125">INPUTS</span></span>

### <span data-ttu-id="e1bcc-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e1bcc-126">System.String</span></span>

### <span data-ttu-id="e1bcc-127">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="e1bcc-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e1bcc-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e1bcc-128">OUTPUTS</span></span>

### <span data-ttu-id="e1bcc-129">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="e1bcc-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="e1bcc-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e1bcc-130">NOTES</span></span>

## <span data-ttu-id="e1bcc-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1bcc-131">RELATED LINKS</span></span>
