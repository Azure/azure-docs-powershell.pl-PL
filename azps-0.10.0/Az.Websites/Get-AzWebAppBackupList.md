---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackupList.md
ms.openlocfilehash: 057bebde5eada143c9ee00260a1406fdceae9436
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891945"
---
# <span data-ttu-id="5c213-101">Get-AzWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="5c213-101">Get-AzWebAppBackupList</span></span>

## <span data-ttu-id="5c213-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5c213-102">SYNOPSIS</span></span>

## <span data-ttu-id="5c213-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5c213-103">SYNTAX</span></span>

### <span data-ttu-id="5c213-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="5c213-104">FromResourceName</span></span>
```
Get-AzWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c213-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="5c213-105">FromWebApp</span></span>
```
Get-AzWebAppBackupList [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c213-106">Opis</span><span class="sxs-lookup"><span data-stu-id="5c213-106">DESCRIPTION</span></span>
<span data-ttu-id="5c213-107">Polecenie cmdlet **Get-AzWebAppBackupList** pobiera listę kopii zapasowych aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="5c213-107">The **Get-AzWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="5c213-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5c213-108">EXAMPLES</span></span>

### <span data-ttu-id="5c213-109">1:1</span><span class="sxs-lookup"><span data-stu-id="5c213-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="5c213-110">To polecenie zwraca listę kopii zapasowych odnoszącą się do aplikacji WebAppStandard skojarzonych z ContosoResourceGroup grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="5c213-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="5c213-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5c213-111">PARAMETERS</span></span>

### <span data-ttu-id="5c213-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c213-112">-DefaultProfile</span></span>
<span data-ttu-id="5c213-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5c213-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c213-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5c213-114">-Name</span></span>
<span data-ttu-id="5c213-115">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="5c213-115">WebApp Name</span></span>

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

### <span data-ttu-id="5c213-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c213-116">-ResourceGroupName</span></span>
<span data-ttu-id="5c213-117">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="5c213-117">Resource Group Name</span></span>

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

### <span data-ttu-id="5c213-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="5c213-118">-Slot</span></span>
<span data-ttu-id="5c213-119">Nazwa gniazda</span><span class="sxs-lookup"><span data-stu-id="5c213-119">Slot name</span></span>

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

### <span data-ttu-id="5c213-120">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="5c213-120">-WebApp</span></span>
<span data-ttu-id="5c213-121">Potok aplikacji</span><span class="sxs-lookup"><span data-stu-id="5c213-121">Piped WebApp</span></span>

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

### <span data-ttu-id="5c213-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c213-122">CommonParameters</span></span>
<span data-ttu-id="5c213-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c213-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c213-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c213-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c213-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c213-125">INPUTS</span></span>

### <span data-ttu-id="5c213-126">Klienta</span><span class="sxs-lookup"><span data-stu-id="5c213-126">Site</span></span>
<span data-ttu-id="5c213-127">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="5c213-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="5c213-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5c213-128">OUTPUTS</span></span>

### <span data-ttu-id="5c213-129">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. webapps. AzureWebAppBackup []</span><span class="sxs-lookup"><span data-stu-id="5c213-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup[]</span></span>

## <span data-ttu-id="5c213-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5c213-130">NOTES</span></span>

## <span data-ttu-id="5c213-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5c213-131">RELATED LINKS</span></span>

