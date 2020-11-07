---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
ms.openlocfilehash: e371beefd521e5a10a4450209393a2f8bdb7b790
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894914"
---
# <span data-ttu-id="52c7f-101">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="52c7f-101">Get-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="52c7f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="52c7f-102">SYNOPSIS</span></span>

## <span data-ttu-id="52c7f-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="52c7f-103">SYNTAX</span></span>

### <span data-ttu-id="52c7f-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="52c7f-104">FromResourceName</span></span>
```
Get-AzWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52c7f-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="52c7f-105">FromWebApp</span></span>
```
Get-AzWebAppBackupConfiguration [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="52c7f-106">Opis</span><span class="sxs-lookup"><span data-stu-id="52c7f-106">DESCRIPTION</span></span>
<span data-ttu-id="52c7f-107">Polecenie cmdlet **Get-AzWebAppBackupConfiguration** Pobiera konfigurację kopii zapasowej aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="52c7f-107">The **Get-AzWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="52c7f-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="52c7f-108">EXAMPLES</span></span>

### <span data-ttu-id="52c7f-109">1:1</span><span class="sxs-lookup"><span data-stu-id="52c7f-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="52c7f-110">To polecenie pobiera konfigurację kopii zapasowej z aplikacji sieci Web o nazwie WebAppStandard należącej do grupy zasobów Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="52c7f-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="52c7f-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="52c7f-111">PARAMETERS</span></span>

### <span data-ttu-id="52c7f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52c7f-112">-DefaultProfile</span></span>
<span data-ttu-id="52c7f-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="52c7f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52c7f-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="52c7f-114">-Name</span></span>
<span data-ttu-id="52c7f-115">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="52c7f-115">WebApp Name</span></span>

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

### <span data-ttu-id="52c7f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52c7f-116">-ResourceGroupName</span></span>
<span data-ttu-id="52c7f-117">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="52c7f-117">Resource Group Name</span></span>

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

### <span data-ttu-id="52c7f-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="52c7f-118">-Slot</span></span>
<span data-ttu-id="52c7f-119">Nazwa gniazda</span><span class="sxs-lookup"><span data-stu-id="52c7f-119">Slot Name</span></span>

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

### <span data-ttu-id="52c7f-120">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="52c7f-120">-WebApp</span></span>
<span data-ttu-id="52c7f-121">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="52c7f-121">WebApp Name</span></span>

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

### <span data-ttu-id="52c7f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52c7f-122">CommonParameters</span></span>
<span data-ttu-id="52c7f-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52c7f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52c7f-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52c7f-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52c7f-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52c7f-125">INPUTS</span></span>

### <span data-ttu-id="52c7f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="52c7f-126">System.String</span></span>

### <span data-ttu-id="52c7f-127">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="52c7f-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="52c7f-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="52c7f-128">OUTPUTS</span></span>

### <span data-ttu-id="52c7f-129">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="52c7f-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="52c7f-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="52c7f-130">NOTES</span></span>

## <span data-ttu-id="52c7f-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="52c7f-131">RELATED LINKS</span></span>
