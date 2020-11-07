---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/start-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Start-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Start-AzWebApp.md
ms.openlocfilehash: d533a2d7401236e374ca6f541e646cb85a080f9b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891825"
---
# <span data-ttu-id="7363a-101">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7363a-101">Start-AzWebApp</span></span>

## <span data-ttu-id="7363a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7363a-102">SYNOPSIS</span></span>
<span data-ttu-id="7363a-103">Uruchamia aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="7363a-103">Starts an Azure Web App.</span></span>

## <span data-ttu-id="7363a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7363a-104">SYNTAX</span></span>

### <span data-ttu-id="7363a-105">S1</span><span class="sxs-lookup"><span data-stu-id="7363a-105">S1</span></span>
```
Start-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7363a-106">S2</span><span class="sxs-lookup"><span data-stu-id="7363a-106">S2</span></span>
```
Start-AzWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7363a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7363a-107">DESCRIPTION</span></span>
<span data-ttu-id="7363a-108">Polecenie cmdlet **Start-AzWebApp** uruchamia aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="7363a-108">The **Start-AzWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="7363a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7363a-109">EXAMPLES</span></span>

### <span data-ttu-id="7363a-110">Przykład 1. Uruchamianie aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="7363a-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="7363a-111">To polecenie uruchamia aplikację sieci Web o nazwie ContosoWebApp należącej do grupy zasobów o nazwie Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="7363a-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="7363a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7363a-112">PARAMETERS</span></span>

### <span data-ttu-id="7363a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7363a-113">-DefaultProfile</span></span>
<span data-ttu-id="7363a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7363a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7363a-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7363a-115">-Name</span></span>
<span data-ttu-id="7363a-116">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="7363a-116">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7363a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7363a-117">-ResourceGroupName</span></span>
<span data-ttu-id="7363a-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7363a-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7363a-119">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="7363a-119">-WebApp</span></span>
<span data-ttu-id="7363a-120">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="7363a-120">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7363a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7363a-121">CommonParameters</span></span>
<span data-ttu-id="7363a-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7363a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7363a-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7363a-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7363a-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7363a-124">INPUTS</span></span>

### <span data-ttu-id="7363a-125">Klienta</span><span class="sxs-lookup"><span data-stu-id="7363a-125">Site</span></span>
<span data-ttu-id="7363a-126">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="7363a-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="7363a-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7363a-127">OUTPUTS</span></span>

## <span data-ttu-id="7363a-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7363a-128">NOTES</span></span>

## <span data-ttu-id="7363a-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7363a-129">RELATED LINKS</span></span>

[<span data-ttu-id="7363a-130">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7363a-130">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="7363a-131">Nowe — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7363a-131">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="7363a-132">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7363a-132">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="7363a-133">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7363a-133">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="7363a-134">Zatrzymaj — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7363a-134">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


