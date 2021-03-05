---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
ms.openlocfilehash: f70caa984fde48db6b2d1d147ebf62f544f2ed9f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972378"
---
# <span data-ttu-id="64dba-101">Get-AzWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="64dba-101">Get-AzWebAppBackupList</span></span>

## <span data-ttu-id="64dba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64dba-102">SYNOPSIS</span></span>

## <span data-ttu-id="64dba-103">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="64dba-103">SYNTAX</span></span>

### <span data-ttu-id="64dba-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="64dba-104">FromResourceName</span></span>
```
Get-AzWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64dba-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="64dba-105">FromWebApp</span></span>
```
Get-AzWebAppBackupList [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64dba-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="64dba-106">DESCRIPTION</span></span>
<span data-ttu-id="64dba-107">Polecenie **cmdlet Get-AzWebAppBackupList** pobiera listę kopii zapasowych dla aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="64dba-107">The **Get-AzWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="64dba-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="64dba-108">EXAMPLES</span></span>

### <span data-ttu-id="64dba-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="64dba-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="64dba-110">To polecenie zwraca listę kopii zapasowej związaną z zasadą WebApp WebApp WebAppStandard skojarzoną z grupą zasobów ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="64dba-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="64dba-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64dba-111">PARAMETERS</span></span>

### <span data-ttu-id="64dba-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64dba-112">-DefaultProfile</span></span>
<span data-ttu-id="64dba-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="64dba-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64dba-114">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="64dba-114">-Name</span></span>
<span data-ttu-id="64dba-115">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="64dba-115">WebApp Name</span></span>

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

### <span data-ttu-id="64dba-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64dba-116">-ResourceGroupName</span></span>
<span data-ttu-id="64dba-117">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="64dba-117">Resource Group Name</span></span>

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

### <span data-ttu-id="64dba-118">— Slot</span><span class="sxs-lookup"><span data-stu-id="64dba-118">-Slot</span></span>
<span data-ttu-id="64dba-119">Nazwa gniazda</span><span class="sxs-lookup"><span data-stu-id="64dba-119">Slot name</span></span>

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

### <span data-ttu-id="64dba-120">- WebApp</span><span class="sxs-lookup"><span data-stu-id="64dba-120">-WebApp</span></span>
<span data-ttu-id="64dba-121">Piped WebApp</span><span class="sxs-lookup"><span data-stu-id="64dba-121">Piped WebApp</span></span>

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

### <span data-ttu-id="64dba-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64dba-122">CommonParameters</span></span>
<span data-ttu-id="64dba-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64dba-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64dba-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64dba-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64dba-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64dba-125">INPUTS</span></span>

### <span data-ttu-id="64dba-126">System.String</span><span class="sxs-lookup"><span data-stu-id="64dba-126">System.String</span></span>

### <span data-ttu-id="64dba-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="64dba-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="64dba-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64dba-128">OUTPUTS</span></span>

### <span data-ttu-id="64dba-129">Microsoft.Azure.Commands.WebApps.Cmdlet.WebApps.AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="64dba-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="64dba-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="64dba-130">NOTES</span></span>

## <span data-ttu-id="64dba-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64dba-131">RELATED LINKS</span></span>
