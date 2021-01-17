---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
ms.openlocfilehash: 33fdfdc1c8b0c4b7bfddbc6b0aafd9ab38ffe701
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491402"
---
# <span data-ttu-id="7174f-101">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7174f-101">Start-AzWebApp</span></span>

## <span data-ttu-id="7174f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7174f-102">SYNOPSIS</span></span>
<span data-ttu-id="7174f-103">Uruchamia aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="7174f-103">Starts an Azure Web App.</span></span>

## <span data-ttu-id="7174f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7174f-104">SYNTAX</span></span>

### <span data-ttu-id="7174f-105">S1</span><span class="sxs-lookup"><span data-stu-id="7174f-105">S1</span></span>
```
Start-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7174f-106">S2</span><span class="sxs-lookup"><span data-stu-id="7174f-106">S2</span></span>
```
Start-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7174f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7174f-107">DESCRIPTION</span></span>
<span data-ttu-id="7174f-108">Polecenie cmdlet **Start-AzWebApp** uruchamia aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="7174f-108">The **Start-AzWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="7174f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7174f-109">EXAMPLES</span></span>

### <span data-ttu-id="7174f-110">Przykład 1. Uruchamianie aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="7174f-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="7174f-111">To polecenie uruchamia aplikację sieci Web o nazwie ContosoWebApp należącej do grupy zasobów o nazwie Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="7174f-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="7174f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7174f-112">PARAMETERS</span></span>

### <span data-ttu-id="7174f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7174f-113">-DefaultProfile</span></span>
<span data-ttu-id="7174f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7174f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7174f-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7174f-115">-Name</span></span>
<span data-ttu-id="7174f-116">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="7174f-116">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7174f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7174f-117">-ResourceGroupName</span></span>
<span data-ttu-id="7174f-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7174f-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7174f-119">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="7174f-119">-WebApp</span></span>
<span data-ttu-id="7174f-120">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="7174f-120">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7174f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7174f-121">CommonParameters</span></span>
<span data-ttu-id="7174f-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7174f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7174f-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7174f-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7174f-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7174f-124">INPUTS</span></span>

### <span data-ttu-id="7174f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="7174f-125">System.String</span></span>

### <span data-ttu-id="7174f-126">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="7174f-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="7174f-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7174f-127">OUTPUTS</span></span>

### <span data-ttu-id="7174f-128">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="7174f-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="7174f-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7174f-129">NOTES</span></span>

## <span data-ttu-id="7174f-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7174f-130">RELATED LINKS</span></span>

[<span data-ttu-id="7174f-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7174f-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="7174f-132">Nowe — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7174f-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="7174f-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7174f-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="7174f-134">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7174f-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="7174f-135">Zatrzymaj — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7174f-135">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


