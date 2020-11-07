---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restart-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebApp.md
ms.openlocfilehash: 7543a1dfbbab0c2cedc59fd8ca0d3b60d78ca69d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716602"
---
# <span data-ttu-id="311f6-101">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="311f6-101">Restart-AzureRmWebApp</span></span>

## <span data-ttu-id="311f6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="311f6-102">SYNOPSIS</span></span>
<span data-ttu-id="311f6-103">Ponownie uruchamia aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="311f6-103">Restarts an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="311f6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="311f6-104">SYNTAX</span></span>

### <span data-ttu-id="311f6-105">S1</span><span class="sxs-lookup"><span data-stu-id="311f6-105">S1</span></span>
```
Restart-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="311f6-106">S2</span><span class="sxs-lookup"><span data-stu-id="311f6-106">S2</span></span>
```
Restart-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="311f6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="311f6-107">DESCRIPTION</span></span>
<span data-ttu-id="311f6-108">Polecenie cmdlet **restart-AzureRmWebApp** zostanie zatrzymane, a następnie zostanie uruchomiona aplikacja Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="311f6-108">The **Restart-AzureRmWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="311f6-109">Jeśli aplikacja sieci Web jest zatrzymana, użyj polecenia cmdlet Start-AzureRmWebApp.</span><span class="sxs-lookup"><span data-stu-id="311f6-109">If the Web App is in a stopped state, use the Start-AzureRmWebApp cmdlet.</span></span>

## <span data-ttu-id="311f6-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="311f6-110">EXAMPLES</span></span>

### <span data-ttu-id="311f6-111">Przykład 1: ponowne uruchamianie aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="311f6-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="311f6-112">To polecenie zatrzymuje aplikację Azure Web App o nazwie ContosoSite, która należy do grupy zasobów o nazwie Default-Web-Zachodnia, a następnie ponownie ją uruchamia.</span><span class="sxs-lookup"><span data-stu-id="311f6-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="311f6-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="311f6-113">PARAMETERS</span></span>

### <span data-ttu-id="311f6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="311f6-114">-DefaultProfile</span></span>
<span data-ttu-id="311f6-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="311f6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="311f6-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="311f6-116">-Name</span></span>
<span data-ttu-id="311f6-117">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="311f6-117">WebApp Name</span></span>

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

### <span data-ttu-id="311f6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="311f6-118">-ResourceGroupName</span></span>
<span data-ttu-id="311f6-119">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="311f6-119">Resource Group Name</span></span>

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

### <span data-ttu-id="311f6-120">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="311f6-120">-WebApp</span></span>
<span data-ttu-id="311f6-121">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="311f6-121">WebApp Object</span></span>

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

### <span data-ttu-id="311f6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="311f6-122">CommonParameters</span></span>
<span data-ttu-id="311f6-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="311f6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="311f6-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="311f6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="311f6-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="311f6-125">INPUTS</span></span>

### <span data-ttu-id="311f6-126">Klienta</span><span class="sxs-lookup"><span data-stu-id="311f6-126">Site</span></span>
<span data-ttu-id="311f6-127">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="311f6-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="311f6-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="311f6-128">OUTPUTS</span></span>

## <span data-ttu-id="311f6-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="311f6-129">NOTES</span></span>

## <span data-ttu-id="311f6-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="311f6-130">RELATED LINKS</span></span>

[<span data-ttu-id="311f6-131">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="311f6-131">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="311f6-132">Nowe — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="311f6-132">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="311f6-133">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="311f6-133">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="311f6-134">Start — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="311f6-134">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="311f6-135">Zatrzymaj — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="311f6-135">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


