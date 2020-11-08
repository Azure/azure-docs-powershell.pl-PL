---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restart-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
ms.openlocfilehash: faa3264dbf9fa65a2970f578c635868d185f2ef8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051880"
---
# <span data-ttu-id="42a17-101">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="42a17-101">Restart-AzWebApp</span></span>

## <span data-ttu-id="42a17-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="42a17-102">SYNOPSIS</span></span>
<span data-ttu-id="42a17-103">Ponownie uruchamia aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="42a17-103">Restarts an Azure Web App.</span></span>

## <span data-ttu-id="42a17-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="42a17-104">SYNTAX</span></span>

### <span data-ttu-id="42a17-105">S1</span><span class="sxs-lookup"><span data-stu-id="42a17-105">S1</span></span>
```
Restart-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="42a17-106">S2</span><span class="sxs-lookup"><span data-stu-id="42a17-106">S2</span></span>
```
Restart-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42a17-107">Opis</span><span class="sxs-lookup"><span data-stu-id="42a17-107">DESCRIPTION</span></span>
<span data-ttu-id="42a17-108">Polecenie cmdlet **restart-AzWebApp** zostanie zatrzymane, a następnie zostanie uruchomiona aplikacja Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="42a17-108">The **Restart-AzWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="42a17-109">Jeśli aplikacja sieci Web jest zatrzymana, użyj polecenia cmdlet Start-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="42a17-109">If the Web App is in a stopped state, use the Start-AzWebApp cmdlet.</span></span>

## <span data-ttu-id="42a17-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="42a17-110">EXAMPLES</span></span>

### <span data-ttu-id="42a17-111">Przykład 1: ponowne uruchamianie aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="42a17-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="42a17-112">To polecenie zatrzymuje aplikację Azure Web App o nazwie ContosoSite, która należy do grupy zasobów o nazwie Default-Web-Zachodnia, a następnie ponownie ją uruchamia.</span><span class="sxs-lookup"><span data-stu-id="42a17-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="42a17-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="42a17-113">PARAMETERS</span></span>

### <span data-ttu-id="42a17-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42a17-114">-DefaultProfile</span></span>
<span data-ttu-id="42a17-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="42a17-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42a17-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="42a17-116">-Name</span></span>
<span data-ttu-id="42a17-117">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="42a17-117">WebApp Name</span></span>

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

### <span data-ttu-id="42a17-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42a17-118">-ResourceGroupName</span></span>
<span data-ttu-id="42a17-119">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="42a17-119">Resource Group Name</span></span>

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

### <span data-ttu-id="42a17-120">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="42a17-120">-WebApp</span></span>
<span data-ttu-id="42a17-121">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="42a17-121">WebApp Object</span></span>

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

### <span data-ttu-id="42a17-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42a17-122">CommonParameters</span></span>
<span data-ttu-id="42a17-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42a17-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42a17-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42a17-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42a17-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42a17-125">INPUTS</span></span>

### <span data-ttu-id="42a17-126">System. String</span><span class="sxs-lookup"><span data-stu-id="42a17-126">System.String</span></span>

### <span data-ttu-id="42a17-127">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="42a17-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="42a17-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="42a17-128">OUTPUTS</span></span>

### <span data-ttu-id="42a17-129">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="42a17-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="42a17-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="42a17-130">NOTES</span></span>

## <span data-ttu-id="42a17-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42a17-131">RELATED LINKS</span></span>

[<span data-ttu-id="42a17-132">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="42a17-132">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="42a17-133">Nowe — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="42a17-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="42a17-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="42a17-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="42a17-135">Start — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="42a17-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="42a17-136">Zatrzymaj — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="42a17-136">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


