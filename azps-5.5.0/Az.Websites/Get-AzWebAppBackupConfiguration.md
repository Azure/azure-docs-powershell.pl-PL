---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 8ef8639c2ff79a326a8d0ffcdf1f1dca24dbccf9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242947"
---
# <span data-ttu-id="ae81c-101">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae81c-101">Get-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="ae81c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae81c-102">SYNOPSIS</span></span>

## <span data-ttu-id="ae81c-103">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ae81c-103">SYNTAX</span></span>

### <span data-ttu-id="ae81c-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="ae81c-104">FromResourceName</span></span>
```
Get-AzWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae81c-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="ae81c-105">FromWebApp</span></span>
```
Get-AzWebAppBackupConfiguration [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ae81c-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="ae81c-106">DESCRIPTION</span></span>
<span data-ttu-id="ae81c-107">Polecenie **cmdlet Get-AzWebAppBackupConfiguration** pobiera konfigurację kopii zapasowej aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ae81c-107">The **Get-AzWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="ae81c-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ae81c-108">EXAMPLES</span></span>

### <span data-ttu-id="ae81c-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ae81c-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="ae81c-110">To polecenie pobiera konfigurację kopii zapasowej z aplikacji Web App o nazwie WebAppStandard, która należy do grupy zasobów Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="ae81c-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="ae81c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae81c-111">PARAMETERS</span></span>

### <span data-ttu-id="ae81c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae81c-112">-DefaultProfile</span></span>
<span data-ttu-id="ae81c-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae81c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae81c-114">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ae81c-114">-Name</span></span>
<span data-ttu-id="ae81c-115">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="ae81c-115">WebApp Name</span></span>

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

### <span data-ttu-id="ae81c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae81c-116">-ResourceGroupName</span></span>
<span data-ttu-id="ae81c-117">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ae81c-117">Resource Group Name</span></span>

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

### <span data-ttu-id="ae81c-118">— Slot</span><span class="sxs-lookup"><span data-stu-id="ae81c-118">-Slot</span></span>
<span data-ttu-id="ae81c-119">Nazwa gniazda</span><span class="sxs-lookup"><span data-stu-id="ae81c-119">Slot Name</span></span>

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

### <span data-ttu-id="ae81c-120">- WebApp</span><span class="sxs-lookup"><span data-stu-id="ae81c-120">-WebApp</span></span>
<span data-ttu-id="ae81c-121">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="ae81c-121">WebApp Name</span></span>

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

### <span data-ttu-id="ae81c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae81c-122">CommonParameters</span></span>
<span data-ttu-id="ae81c-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae81c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae81c-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae81c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae81c-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae81c-125">INPUTS</span></span>

### <span data-ttu-id="ae81c-126">System.String</span><span class="sxs-lookup"><span data-stu-id="ae81c-126">System.String</span></span>

### <span data-ttu-id="ae81c-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="ae81c-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ae81c-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae81c-128">OUTPUTS</span></span>

### <span data-ttu-id="ae81c-129">Microsoft.Azure.Commands.WebApps.Cmdlet.WebApps.AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae81c-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="ae81c-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ae81c-130">NOTES</span></span>

## <span data-ttu-id="ae81c-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae81c-131">RELATED LINKS</span></span>
