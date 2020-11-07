---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupList.md
ms.openlocfilehash: 0f8192441b3bf555145da8259f369a9091193800
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716604"
---
# <span data-ttu-id="9ab12-101">Get-AzureRmWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="9ab12-101">Get-AzureRmWebAppBackupList</span></span>

## <span data-ttu-id="9ab12-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9ab12-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ab12-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9ab12-103">SYNTAX</span></span>

### <span data-ttu-id="9ab12-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="9ab12-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ab12-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="9ab12-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupList [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ab12-106">Opis</span><span class="sxs-lookup"><span data-stu-id="9ab12-106">DESCRIPTION</span></span>
<span data-ttu-id="9ab12-107">Polecenie cmdlet **Get-AzureRmWebAppBackupList** pobiera listę kopii zapasowych aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="9ab12-107">The **Get-AzureRmWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="9ab12-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9ab12-108">EXAMPLES</span></span>

### <span data-ttu-id="9ab12-109">1:1</span><span class="sxs-lookup"><span data-stu-id="9ab12-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="9ab12-110">To polecenie zwraca listę kopii zapasowych odnoszącą się do aplikacji WebAppStandard skojarzonych z ContosoResourceGroup grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="9ab12-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="9ab12-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9ab12-111">PARAMETERS</span></span>

### <span data-ttu-id="9ab12-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ab12-112">-DefaultProfile</span></span>
<span data-ttu-id="9ab12-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9ab12-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ab12-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9ab12-114">-Name</span></span>
<span data-ttu-id="9ab12-115">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="9ab12-115">WebApp Name</span></span>

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

### <span data-ttu-id="9ab12-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ab12-116">-ResourceGroupName</span></span>
<span data-ttu-id="9ab12-117">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="9ab12-117">Resource Group Name</span></span>

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

### <span data-ttu-id="9ab12-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="9ab12-118">-Slot</span></span>
<span data-ttu-id="9ab12-119">Nazwa gniazda</span><span class="sxs-lookup"><span data-stu-id="9ab12-119">Slot name</span></span>

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

### <span data-ttu-id="9ab12-120">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="9ab12-120">-WebApp</span></span>
<span data-ttu-id="9ab12-121">Potok aplikacji</span><span class="sxs-lookup"><span data-stu-id="9ab12-121">Piped WebApp</span></span>

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

### <span data-ttu-id="9ab12-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ab12-122">CommonParameters</span></span>
<span data-ttu-id="9ab12-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ab12-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ab12-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ab12-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ab12-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ab12-125">INPUTS</span></span>

### <span data-ttu-id="9ab12-126">Klienta</span><span class="sxs-lookup"><span data-stu-id="9ab12-126">Site</span></span>
<span data-ttu-id="9ab12-127">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="9ab12-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="9ab12-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9ab12-128">OUTPUTS</span></span>

### <span data-ttu-id="9ab12-129">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. webapps. AzureWebAppBackup []</span><span class="sxs-lookup"><span data-stu-id="9ab12-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup[]</span></span>

## <span data-ttu-id="9ab12-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9ab12-130">NOTES</span></span>

## <span data-ttu-id="9ab12-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9ab12-131">RELATED LINKS</span></span>

