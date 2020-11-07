---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
ms.openlocfilehash: 104614bd0fdd2ca8555765a301f6b257cdac0bc7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894902"
---
# <span data-ttu-id="b6a41-101">Get-AzWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="b6a41-101">Get-AzWebAppBackupList</span></span>

## <span data-ttu-id="b6a41-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6a41-102">SYNOPSIS</span></span>

## <span data-ttu-id="b6a41-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6a41-103">SYNTAX</span></span>

### <span data-ttu-id="b6a41-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="b6a41-104">FromResourceName</span></span>
```
Get-AzWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6a41-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="b6a41-105">FromWebApp</span></span>
```
Get-AzWebAppBackupList [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6a41-106">Opis</span><span class="sxs-lookup"><span data-stu-id="b6a41-106">DESCRIPTION</span></span>
<span data-ttu-id="b6a41-107">Polecenie cmdlet **Get-AzWebAppBackupList** pobiera listę kopii zapasowych aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="b6a41-107">The **Get-AzWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="b6a41-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6a41-108">EXAMPLES</span></span>

### <span data-ttu-id="b6a41-109">1:1</span><span class="sxs-lookup"><span data-stu-id="b6a41-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="b6a41-110">To polecenie zwraca listę kopii zapasowych odnoszącą się do aplikacji WebAppStandard skojarzonych z ContosoResourceGroup grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="b6a41-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="b6a41-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6a41-111">PARAMETERS</span></span>

### <span data-ttu-id="b6a41-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6a41-112">-DefaultProfile</span></span>
<span data-ttu-id="b6a41-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b6a41-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6a41-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b6a41-114">-Name</span></span>
<span data-ttu-id="b6a41-115">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="b6a41-115">WebApp Name</span></span>

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

### <span data-ttu-id="b6a41-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6a41-116">-ResourceGroupName</span></span>
<span data-ttu-id="b6a41-117">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b6a41-117">Resource Group Name</span></span>

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

### <span data-ttu-id="b6a41-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="b6a41-118">-Slot</span></span>
<span data-ttu-id="b6a41-119">Nazwa gniazda</span><span class="sxs-lookup"><span data-stu-id="b6a41-119">Slot name</span></span>

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

### <span data-ttu-id="b6a41-120">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="b6a41-120">-WebApp</span></span>
<span data-ttu-id="b6a41-121">Potok aplikacji</span><span class="sxs-lookup"><span data-stu-id="b6a41-121">Piped WebApp</span></span>

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

### <span data-ttu-id="b6a41-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6a41-122">CommonParameters</span></span>
<span data-ttu-id="b6a41-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6a41-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6a41-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6a41-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6a41-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6a41-125">INPUTS</span></span>

### <span data-ttu-id="b6a41-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b6a41-126">System.String</span></span>

### <span data-ttu-id="b6a41-127">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="b6a41-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b6a41-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6a41-128">OUTPUTS</span></span>

### <span data-ttu-id="b6a41-129">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="b6a41-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="b6a41-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6a41-130">NOTES</span></span>

## <span data-ttu-id="b6a41-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6a41-131">RELATED LINKS</span></span>
