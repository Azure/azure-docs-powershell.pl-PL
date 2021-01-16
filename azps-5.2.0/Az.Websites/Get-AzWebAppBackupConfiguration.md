---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 8ef8639c2ff79a326a8d0ffcdf1f1dca24dbccf9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326900"
---
# <span data-ttu-id="d2785-101">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2785-101">Get-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="d2785-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d2785-102">SYNOPSIS</span></span>

## <span data-ttu-id="d2785-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d2785-103">SYNTAX</span></span>

### <span data-ttu-id="d2785-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="d2785-104">FromResourceName</span></span>
```
Get-AzWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2785-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="d2785-105">FromWebApp</span></span>
```
Get-AzWebAppBackupConfiguration [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d2785-106">Opis</span><span class="sxs-lookup"><span data-stu-id="d2785-106">DESCRIPTION</span></span>
<span data-ttu-id="d2785-107">Polecenie cmdlet **Get-AzWebAppBackupConfiguration** Pobiera konfigurację kopii zapasowej aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="d2785-107">The **Get-AzWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="d2785-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d2785-108">EXAMPLES</span></span>

### <span data-ttu-id="d2785-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d2785-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="d2785-110">To polecenie pobiera konfigurację kopii zapasowej z aplikacji sieci Web o nazwie WebAppStandard należącej do grupy zasobów Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="d2785-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="d2785-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d2785-111">PARAMETERS</span></span>

### <span data-ttu-id="d2785-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2785-112">-DefaultProfile</span></span>
<span data-ttu-id="d2785-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d2785-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2785-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d2785-114">-Name</span></span>
<span data-ttu-id="d2785-115">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="d2785-115">WebApp Name</span></span>

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

### <span data-ttu-id="d2785-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2785-116">-ResourceGroupName</span></span>
<span data-ttu-id="d2785-117">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d2785-117">Resource Group Name</span></span>

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

### <span data-ttu-id="d2785-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="d2785-118">-Slot</span></span>
<span data-ttu-id="d2785-119">Nazwa gniazda</span><span class="sxs-lookup"><span data-stu-id="d2785-119">Slot Name</span></span>

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

### <span data-ttu-id="d2785-120">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="d2785-120">-WebApp</span></span>
<span data-ttu-id="d2785-121">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="d2785-121">WebApp Name</span></span>

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

### <span data-ttu-id="d2785-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2785-122">CommonParameters</span></span>
<span data-ttu-id="d2785-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2785-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2785-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2785-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2785-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2785-125">INPUTS</span></span>

### <span data-ttu-id="d2785-126">System. String</span><span class="sxs-lookup"><span data-stu-id="d2785-126">System.String</span></span>

### <span data-ttu-id="d2785-127">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="d2785-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d2785-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d2785-128">OUTPUTS</span></span>

### <span data-ttu-id="d2785-129">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2785-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="d2785-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d2785-130">NOTES</span></span>

## <span data-ttu-id="d2785-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2785-131">RELATED LINKS</span></span>
