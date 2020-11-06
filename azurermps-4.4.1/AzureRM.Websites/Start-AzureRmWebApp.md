---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebApp.md
ms.openlocfilehash: 20acba9bc0f08857c9bdfaaf559544f26b4902ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525442"
---
# <span data-ttu-id="82c23-101">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="82c23-101">Start-AzureRmWebApp</span></span>

## <span data-ttu-id="82c23-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="82c23-102">SYNOPSIS</span></span>
<span data-ttu-id="82c23-103">Uruchamia aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="82c23-103">Starts an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82c23-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="82c23-104">SYNTAX</span></span>

### <span data-ttu-id="82c23-105">S1</span><span class="sxs-lookup"><span data-stu-id="82c23-105">S1</span></span>
```
Start-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="82c23-106">S2</span><span class="sxs-lookup"><span data-stu-id="82c23-106">S2</span></span>
```
Start-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82c23-107">Opis</span><span class="sxs-lookup"><span data-stu-id="82c23-107">DESCRIPTION</span></span>
<span data-ttu-id="82c23-108">Polecenie cmdlet **Start-AzureRmWebApp** uruchamia aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="82c23-108">The **Start-AzureRmWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="82c23-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="82c23-109">EXAMPLES</span></span>

### <span data-ttu-id="82c23-110">Przykład 1. Uruchamianie aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="82c23-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="82c23-111">To polecenie uruchamia aplikację sieci Web o nazwie ContosoWebApp należącej do grupy zasobów o nazwie Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="82c23-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="82c23-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="82c23-112">PARAMETERS</span></span>

### <span data-ttu-id="82c23-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="82c23-113">-Name</span></span>
<span data-ttu-id="82c23-114">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="82c23-114">WebApp Name</span></span>

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

### <span data-ttu-id="82c23-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82c23-115">-ResourceGroupName</span></span>
<span data-ttu-id="82c23-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="82c23-116">Resource Group Name</span></span>

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

### <span data-ttu-id="82c23-117">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="82c23-117">-WebApp</span></span>
<span data-ttu-id="82c23-118">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="82c23-118">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82c23-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82c23-119">-DefaultProfile</span></span>
<span data-ttu-id="82c23-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="82c23-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82c23-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82c23-121">CommonParameters</span></span>
<span data-ttu-id="82c23-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82c23-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82c23-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82c23-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82c23-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="82c23-124">INPUTS</span></span>

### <span data-ttu-id="82c23-125">Klienta</span><span class="sxs-lookup"><span data-stu-id="82c23-125">Site</span></span>
<span data-ttu-id="82c23-126">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="82c23-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="82c23-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="82c23-127">OUTPUTS</span></span>

## <span data-ttu-id="82c23-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="82c23-128">NOTES</span></span>

## <span data-ttu-id="82c23-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="82c23-129">RELATED LINKS</span></span>

[<span data-ttu-id="82c23-130">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="82c23-130">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="82c23-131">Nowe — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="82c23-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="82c23-132">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="82c23-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="82c23-133">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="82c23-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="82c23-134">Zatrzymaj — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="82c23-134">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


