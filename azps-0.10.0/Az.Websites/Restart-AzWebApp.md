---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/restart-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restart-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restart-AzWebApp.md
ms.openlocfilehash: 975b49af1e20c5b9f4839a561494eaeb8275f02f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891842"
---
# <span data-ttu-id="e44d7-101">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e44d7-101">Restart-AzWebApp</span></span>

## <span data-ttu-id="e44d7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e44d7-102">SYNOPSIS</span></span>
<span data-ttu-id="e44d7-103">Ponownie uruchamia aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="e44d7-103">Restarts an Azure Web App.</span></span>

## <span data-ttu-id="e44d7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e44d7-104">SYNTAX</span></span>

### <span data-ttu-id="e44d7-105">S1</span><span class="sxs-lookup"><span data-stu-id="e44d7-105">S1</span></span>
```
Restart-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e44d7-106">S2</span><span class="sxs-lookup"><span data-stu-id="e44d7-106">S2</span></span>
```
Restart-AzWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e44d7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e44d7-107">DESCRIPTION</span></span>
<span data-ttu-id="e44d7-108">Polecenie cmdlet **restart-AzWebApp** zostanie zatrzymane, a następnie zostanie uruchomiona aplikacja Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="e44d7-108">The **Restart-AzWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="e44d7-109">Jeśli aplikacja sieci Web jest zatrzymana, użyj polecenia cmdlet Start-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="e44d7-109">If the Web App is in a stopped state, use the Start-AzWebApp cmdlet.</span></span>

## <span data-ttu-id="e44d7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e44d7-110">EXAMPLES</span></span>

### <span data-ttu-id="e44d7-111">Przykład 1: ponowne uruchamianie aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="e44d7-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="e44d7-112">To polecenie zatrzymuje aplikację Azure Web App o nazwie ContosoSite, która należy do grupy zasobów o nazwie Default-Web-Zachodnia, a następnie ponownie ją uruchamia.</span><span class="sxs-lookup"><span data-stu-id="e44d7-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="e44d7-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e44d7-113">PARAMETERS</span></span>

### <span data-ttu-id="e44d7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e44d7-114">-DefaultProfile</span></span>
<span data-ttu-id="e44d7-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e44d7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e44d7-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e44d7-116">-Name</span></span>
<span data-ttu-id="e44d7-117">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="e44d7-117">WebApp Name</span></span>

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

### <span data-ttu-id="e44d7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e44d7-118">-ResourceGroupName</span></span>
<span data-ttu-id="e44d7-119">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e44d7-119">Resource Group Name</span></span>

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

### <span data-ttu-id="e44d7-120">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="e44d7-120">-WebApp</span></span>
<span data-ttu-id="e44d7-121">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="e44d7-121">WebApp Object</span></span>

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

### <span data-ttu-id="e44d7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e44d7-122">CommonParameters</span></span>
<span data-ttu-id="e44d7-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e44d7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e44d7-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e44d7-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e44d7-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e44d7-125">INPUTS</span></span>

### <span data-ttu-id="e44d7-126">Klienta</span><span class="sxs-lookup"><span data-stu-id="e44d7-126">Site</span></span>
<span data-ttu-id="e44d7-127">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="e44d7-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="e44d7-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e44d7-128">OUTPUTS</span></span>

## <span data-ttu-id="e44d7-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e44d7-129">NOTES</span></span>

## <span data-ttu-id="e44d7-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e44d7-130">RELATED LINKS</span></span>

[<span data-ttu-id="e44d7-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e44d7-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="e44d7-132">Nowe — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e44d7-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="e44d7-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e44d7-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="e44d7-134">Start — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e44d7-134">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="e44d7-135">Zatrzymaj — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e44d7-135">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


