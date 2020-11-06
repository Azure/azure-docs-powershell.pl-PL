---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupList.md
ms.openlocfilehash: f4005df31746b63b2a45fa2c78f254e2d5f24c59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525889"
---
# <span data-ttu-id="789a9-101">Get-AzureRmWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="789a9-101">Get-AzureRmWebAppBackupList</span></span>

## <span data-ttu-id="789a9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="789a9-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="789a9-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="789a9-103">SYNTAX</span></span>

### <span data-ttu-id="789a9-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="789a9-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="789a9-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="789a9-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupList [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="789a9-106">Opis</span><span class="sxs-lookup"><span data-stu-id="789a9-106">DESCRIPTION</span></span>
<span data-ttu-id="789a9-107">Polecenie cmdlet **Get-AzureRmWebAppBackupList** pobiera listę kopii zapasowych aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="789a9-107">The **Get-AzureRmWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="789a9-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="789a9-108">EXAMPLES</span></span>

### <span data-ttu-id="789a9-109">1:1</span><span class="sxs-lookup"><span data-stu-id="789a9-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="789a9-110">To polecenie zwraca listę kopii zapasowych odnoszącą się do aplikacji WebAppStandard skojarzonych z ContosoResourceGroup grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="789a9-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="789a9-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="789a9-111">PARAMETERS</span></span>

### <span data-ttu-id="789a9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="789a9-112">-DefaultProfile</span></span>
<span data-ttu-id="789a9-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="789a9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="789a9-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="789a9-114">-Name</span></span>
<span data-ttu-id="789a9-115">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="789a9-115">WebApp Name</span></span>

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

### <span data-ttu-id="789a9-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="789a9-116">-ResourceGroupName</span></span>
<span data-ttu-id="789a9-117">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="789a9-117">Resource Group Name</span></span>

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

### <span data-ttu-id="789a9-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="789a9-118">-Slot</span></span>
<span data-ttu-id="789a9-119">Nazwa gniazda</span><span class="sxs-lookup"><span data-stu-id="789a9-119">Slot name</span></span>

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

### <span data-ttu-id="789a9-120">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="789a9-120">-WebApp</span></span>
<span data-ttu-id="789a9-121">Potok aplikacji</span><span class="sxs-lookup"><span data-stu-id="789a9-121">Piped WebApp</span></span>

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

### <span data-ttu-id="789a9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="789a9-122">CommonParameters</span></span>
<span data-ttu-id="789a9-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="789a9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="789a9-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="789a9-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="789a9-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="789a9-125">INPUTS</span></span>

### <span data-ttu-id="789a9-126">System. String</span><span class="sxs-lookup"><span data-stu-id="789a9-126">System.String</span></span>

### <span data-ttu-id="789a9-127">Microsoft. Azure. Management. Web. models. site</span><span class="sxs-lookup"><span data-stu-id="789a9-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="789a9-128">Parametry: aplikacji (ByValue)</span><span class="sxs-lookup"><span data-stu-id="789a9-128">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="789a9-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="789a9-129">OUTPUTS</span></span>

### <span data-ttu-id="789a9-130">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="789a9-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="789a9-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="789a9-131">NOTES</span></span>

## <span data-ttu-id="789a9-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="789a9-132">RELATED LINKS</span></span>
