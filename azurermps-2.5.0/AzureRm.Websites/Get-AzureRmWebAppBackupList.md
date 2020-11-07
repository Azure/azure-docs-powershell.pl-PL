---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackuplist
schema: 2.0.0
ms.openlocfilehash: ef409c62d56a95d36f1e7c9a02018b281c00e3c9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897769"
---
# <span data-ttu-id="97032-101">Get-AzureRmWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="97032-101">Get-AzureRmWebAppBackupList</span></span>

## <span data-ttu-id="97032-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="97032-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97032-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="97032-103">SYNTAX</span></span>

### <span data-ttu-id="97032-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="97032-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97032-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="97032-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupList [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97032-106">Opis</span><span class="sxs-lookup"><span data-stu-id="97032-106">DESCRIPTION</span></span>
<span data-ttu-id="97032-107">Polecenie cmdlet **Get-AzureRmWebAppBackupList** pobiera listę kopii zapasowych aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="97032-107">The **Get-AzureRmWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="97032-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="97032-108">EXAMPLES</span></span>

### <span data-ttu-id="97032-109">1:1</span><span class="sxs-lookup"><span data-stu-id="97032-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="97032-110">To polecenie zwraca listę kopii zapasowych odnoszącą się do aplikacji WebAppStandard skojarzonych z ContosoResourceGroup grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="97032-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="97032-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="97032-111">PARAMETERS</span></span>

### <span data-ttu-id="97032-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97032-112">-DefaultProfile</span></span>
<span data-ttu-id="97032-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="97032-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97032-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="97032-114">-Name</span></span>
<span data-ttu-id="97032-115">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="97032-115">WebApp Name</span></span>

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

### <span data-ttu-id="97032-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97032-116">-ResourceGroupName</span></span>
<span data-ttu-id="97032-117">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="97032-117">Resource Group Name</span></span>

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

### <span data-ttu-id="97032-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="97032-118">-Slot</span></span>
<span data-ttu-id="97032-119">Nazwa gniazda</span><span class="sxs-lookup"><span data-stu-id="97032-119">Slot name</span></span>

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

### <span data-ttu-id="97032-120">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="97032-120">-WebApp</span></span>
<span data-ttu-id="97032-121">Potok aplikacji</span><span class="sxs-lookup"><span data-stu-id="97032-121">Piped WebApp</span></span>

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

### <span data-ttu-id="97032-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97032-122">CommonParameters</span></span>
<span data-ttu-id="97032-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97032-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97032-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97032-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97032-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97032-125">INPUTS</span></span>

### <span data-ttu-id="97032-126">Klienta</span><span class="sxs-lookup"><span data-stu-id="97032-126">Site</span></span>
<span data-ttu-id="97032-127">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="97032-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="97032-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="97032-128">OUTPUTS</span></span>

### <span data-ttu-id="97032-129">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. webapps. AzureWebAppBackup []</span><span class="sxs-lookup"><span data-stu-id="97032-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup[]</span></span>

## <span data-ttu-id="97032-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="97032-130">NOTES</span></span>

## <span data-ttu-id="97032-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="97032-131">RELATED LINKS</span></span>

