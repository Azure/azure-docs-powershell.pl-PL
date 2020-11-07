---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupList.md
ms.openlocfilehash: 02c83e79b5f56d4ef9a6d7730efb5cf5c42a9da8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717541"
---
# <span data-ttu-id="926e7-101">Get-AzureRmWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="926e7-101">Get-AzureRmWebAppBackupList</span></span>

## <span data-ttu-id="926e7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="926e7-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="926e7-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="926e7-103">SYNTAX</span></span>

### <span data-ttu-id="926e7-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="926e7-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="926e7-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="926e7-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupList [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="926e7-106">Opis</span><span class="sxs-lookup"><span data-stu-id="926e7-106">DESCRIPTION</span></span>
<span data-ttu-id="926e7-107">Polecenie cmdlet **Get-AzureRmWebAppBackupList** pobiera listę kopii zapasowych aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="926e7-107">The **Get-AzureRmWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="926e7-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="926e7-108">EXAMPLES</span></span>

### <span data-ttu-id="926e7-109">1:1</span><span class="sxs-lookup"><span data-stu-id="926e7-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="926e7-110">To polecenie zwraca listę kopii zapasowych odnoszącą się do aplikacji WebAppStandard skojarzonych z ContosoResourceGroup grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="926e7-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="926e7-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="926e7-111">PARAMETERS</span></span>

### <span data-ttu-id="926e7-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="926e7-112">-Name</span></span>
<span data-ttu-id="926e7-113">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="926e7-113">WebApp Name</span></span>

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

### <span data-ttu-id="926e7-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="926e7-114">-ResourceGroupName</span></span>
<span data-ttu-id="926e7-115">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="926e7-115">Resource Group Name</span></span>

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

### <span data-ttu-id="926e7-116">-Slot</span><span class="sxs-lookup"><span data-stu-id="926e7-116">-Slot</span></span>
<span data-ttu-id="926e7-117">Nazwa gniazda</span><span class="sxs-lookup"><span data-stu-id="926e7-117">Slot name</span></span>

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

### <span data-ttu-id="926e7-118">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="926e7-118">-WebApp</span></span>
<span data-ttu-id="926e7-119">Potok aplikacji</span><span class="sxs-lookup"><span data-stu-id="926e7-119">Piped WebApp</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="926e7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="926e7-120">-DefaultProfile</span></span>
<span data-ttu-id="926e7-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="926e7-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="926e7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="926e7-122">CommonParameters</span></span>
<span data-ttu-id="926e7-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="926e7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="926e7-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="926e7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="926e7-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="926e7-125">INPUTS</span></span>

### <span data-ttu-id="926e7-126">Klienta</span><span class="sxs-lookup"><span data-stu-id="926e7-126">Site</span></span>
<span data-ttu-id="926e7-127">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="926e7-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="926e7-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="926e7-128">OUTPUTS</span></span>

### <span data-ttu-id="926e7-129">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. webapps. AzureWebAppBackup []</span><span class="sxs-lookup"><span data-stu-id="926e7-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup[]</span></span>

## <span data-ttu-id="926e7-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="926e7-130">NOTES</span></span>

## <span data-ttu-id="926e7-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="926e7-131">RELATED LINKS</span></span>

