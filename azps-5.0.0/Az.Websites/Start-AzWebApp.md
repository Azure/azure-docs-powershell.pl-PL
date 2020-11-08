---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
ms.openlocfilehash: 33fdfdc1c8b0c4b7bfddbc6b0aafd9ab38ffe701
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232439"
---
# <span data-ttu-id="8ef49-101">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8ef49-101">Start-AzWebApp</span></span>

## <span data-ttu-id="8ef49-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8ef49-102">SYNOPSIS</span></span>
<span data-ttu-id="8ef49-103">Uruchamia aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="8ef49-103">Starts an Azure Web App.</span></span>

## <span data-ttu-id="8ef49-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8ef49-104">SYNTAX</span></span>

### <span data-ttu-id="8ef49-105">S1</span><span class="sxs-lookup"><span data-stu-id="8ef49-105">S1</span></span>
```
Start-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ef49-106">S2</span><span class="sxs-lookup"><span data-stu-id="8ef49-106">S2</span></span>
```
Start-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ef49-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8ef49-107">DESCRIPTION</span></span>
<span data-ttu-id="8ef49-108">Polecenie cmdlet **Start-AzWebApp** uruchamia aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="8ef49-108">The **Start-AzWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="8ef49-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8ef49-109">EXAMPLES</span></span>

### <span data-ttu-id="8ef49-110">Przykład 1. Uruchamianie aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="8ef49-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="8ef49-111">To polecenie uruchamia aplikację sieci Web o nazwie ContosoWebApp należącej do grupy zasobów o nazwie Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="8ef49-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="8ef49-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8ef49-112">PARAMETERS</span></span>

### <span data-ttu-id="8ef49-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ef49-113">-DefaultProfile</span></span>
<span data-ttu-id="8ef49-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8ef49-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ef49-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8ef49-115">-Name</span></span>
<span data-ttu-id="8ef49-116">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="8ef49-116">WebApp Name</span></span>

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

### <span data-ttu-id="8ef49-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ef49-117">-ResourceGroupName</span></span>
<span data-ttu-id="8ef49-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8ef49-118">Resource Group Name</span></span>

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

### <span data-ttu-id="8ef49-119">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="8ef49-119">-WebApp</span></span>
<span data-ttu-id="8ef49-120">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="8ef49-120">WebApp Object</span></span>

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

### <span data-ttu-id="8ef49-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ef49-121">CommonParameters</span></span>
<span data-ttu-id="8ef49-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ef49-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ef49-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ef49-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ef49-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ef49-124">INPUTS</span></span>

### <span data-ttu-id="8ef49-125">System. String</span><span class="sxs-lookup"><span data-stu-id="8ef49-125">System.String</span></span>

### <span data-ttu-id="8ef49-126">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="8ef49-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8ef49-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8ef49-127">OUTPUTS</span></span>

### <span data-ttu-id="8ef49-128">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="8ef49-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8ef49-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8ef49-129">NOTES</span></span>

## <span data-ttu-id="8ef49-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ef49-130">RELATED LINKS</span></span>

[<span data-ttu-id="8ef49-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8ef49-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="8ef49-132">Nowe — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8ef49-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="8ef49-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8ef49-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="8ef49-134">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8ef49-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="8ef49-135">Zatrzymaj — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8ef49-135">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


