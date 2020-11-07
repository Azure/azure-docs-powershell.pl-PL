---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/stop-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebApp.md
ms.openlocfilehash: 073c98abe9db8b8a8d52c6d9bb06e64b028d379b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891797"
---
# <span data-ttu-id="e27d9-101">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e27d9-101">Stop-AzWebApp</span></span>

## <span data-ttu-id="e27d9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e27d9-102">SYNOPSIS</span></span>
<span data-ttu-id="e27d9-103">Zatrzymuje aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="e27d9-103">Stops an Azure Web App.</span></span>

## <span data-ttu-id="e27d9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e27d9-104">SYNTAX</span></span>

### <span data-ttu-id="e27d9-105">S1</span><span class="sxs-lookup"><span data-stu-id="e27d9-105">S1</span></span>
```
Stop-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e27d9-106">S2</span><span class="sxs-lookup"><span data-stu-id="e27d9-106">S2</span></span>
```
Stop-AzWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e27d9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e27d9-107">DESCRIPTION</span></span>
<span data-ttu-id="e27d9-108">Polecenie cmdlet **stop-AzWebApp** zatrzymuje aplikację sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e27d9-108">The **Stop-AzWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="e27d9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e27d9-109">EXAMPLES</span></span>

### <span data-ttu-id="e27d9-110">Przykład 1: zatrzymywanie aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="e27d9-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="e27d9-111">To polecenie zatrzymuje aplikację sieci Web o nazwie ContosoWebApp należącej do grupy zasobów o nazwie Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="e27d9-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="e27d9-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e27d9-112">PARAMETERS</span></span>

### <span data-ttu-id="e27d9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e27d9-113">-DefaultProfile</span></span>
<span data-ttu-id="e27d9-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e27d9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e27d9-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e27d9-115">-Name</span></span>
<span data-ttu-id="e27d9-116">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="e27d9-116">WebApp Name</span></span>

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

### <span data-ttu-id="e27d9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e27d9-117">-ResourceGroupName</span></span>
<span data-ttu-id="e27d9-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e27d9-118">Resource Group Name</span></span>

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

### <span data-ttu-id="e27d9-119">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="e27d9-119">-WebApp</span></span>
<span data-ttu-id="e27d9-120">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="e27d9-120">WebApp Object</span></span>

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

### <span data-ttu-id="e27d9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e27d9-121">CommonParameters</span></span>
<span data-ttu-id="e27d9-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e27d9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e27d9-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e27d9-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e27d9-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e27d9-124">INPUTS</span></span>

### <span data-ttu-id="e27d9-125">Klienta</span><span class="sxs-lookup"><span data-stu-id="e27d9-125">Site</span></span>
<span data-ttu-id="e27d9-126">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="e27d9-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="e27d9-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e27d9-127">OUTPUTS</span></span>

## <span data-ttu-id="e27d9-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e27d9-128">NOTES</span></span>

## <span data-ttu-id="e27d9-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e27d9-129">RELATED LINKS</span></span>

[<span data-ttu-id="e27d9-130">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e27d9-130">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="e27d9-131">Nowe — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e27d9-131">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="e27d9-132">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e27d9-132">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="e27d9-133">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e27d9-133">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="e27d9-134">Start — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e27d9-134">Start-AzWebApp</span></span>](./Start-AzWebApp.md)


