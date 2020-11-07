---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
ms.openlocfilehash: fab8973c63e419cdef45fb79a0ad5182c46f2de5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888514"
---
# <span data-ttu-id="57ebf-101">Get-AzWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="57ebf-101">Get-AzWebAppBackupList</span></span>

## <span data-ttu-id="57ebf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="57ebf-102">SYNOPSIS</span></span>

## <span data-ttu-id="57ebf-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="57ebf-103">SYNTAX</span></span>

### <span data-ttu-id="57ebf-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="57ebf-104">FromResourceName</span></span>
```
Get-AzWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57ebf-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="57ebf-105">FromWebApp</span></span>
```
Get-AzWebAppBackupList [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57ebf-106">Opis</span><span class="sxs-lookup"><span data-stu-id="57ebf-106">DESCRIPTION</span></span>
<span data-ttu-id="57ebf-107">Polecenie cmdlet **Get-AzWebAppBackupList** pobiera listę kopii zapasowych aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="57ebf-107">The **Get-AzWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="57ebf-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="57ebf-108">EXAMPLES</span></span>

### <span data-ttu-id="57ebf-109">1:1</span><span class="sxs-lookup"><span data-stu-id="57ebf-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="57ebf-110">To polecenie zwraca listę kopii zapasowych odnoszącą się do aplikacji WebAppStandard skojarzonych z ContosoResourceGroup grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="57ebf-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="57ebf-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="57ebf-111">PARAMETERS</span></span>

### <span data-ttu-id="57ebf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57ebf-112">-DefaultProfile</span></span>
<span data-ttu-id="57ebf-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="57ebf-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57ebf-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="57ebf-114">-Name</span></span>
<span data-ttu-id="57ebf-115">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="57ebf-115">WebApp Name</span></span>

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

### <span data-ttu-id="57ebf-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57ebf-116">-ResourceGroupName</span></span>
<span data-ttu-id="57ebf-117">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="57ebf-117">Resource Group Name</span></span>

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

### <span data-ttu-id="57ebf-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="57ebf-118">-Slot</span></span>
<span data-ttu-id="57ebf-119">Nazwa gniazda</span><span class="sxs-lookup"><span data-stu-id="57ebf-119">Slot name</span></span>

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

### <span data-ttu-id="57ebf-120">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="57ebf-120">-WebApp</span></span>
<span data-ttu-id="57ebf-121">Potok aplikacji</span><span class="sxs-lookup"><span data-stu-id="57ebf-121">Piped WebApp</span></span>

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

### <span data-ttu-id="57ebf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57ebf-122">CommonParameters</span></span>
<span data-ttu-id="57ebf-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57ebf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57ebf-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57ebf-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57ebf-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57ebf-125">INPUTS</span></span>

### <span data-ttu-id="57ebf-126">System. String</span><span class="sxs-lookup"><span data-stu-id="57ebf-126">System.String</span></span>

### <span data-ttu-id="57ebf-127">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="57ebf-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="57ebf-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="57ebf-128">OUTPUTS</span></span>

### <span data-ttu-id="57ebf-129">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="57ebf-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="57ebf-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="57ebf-130">NOTES</span></span>

## <span data-ttu-id="57ebf-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57ebf-131">RELATED LINKS</span></span>
