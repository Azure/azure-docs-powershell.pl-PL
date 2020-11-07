---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restart-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: 775c82585d31e223b3f769cccc458e1523f42b62
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899019"
---
# <span data-ttu-id="8e7fc-101">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="8e7fc-101">Restart-AzureRmWebApp</span></span>

## <span data-ttu-id="8e7fc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8e7fc-102">SYNOPSIS</span></span>
<span data-ttu-id="8e7fc-103">Ponownie uruchamia aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="8e7fc-103">Restarts an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e7fc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8e7fc-104">SYNTAX</span></span>

### <span data-ttu-id="8e7fc-105">S1</span><span class="sxs-lookup"><span data-stu-id="8e7fc-105">S1</span></span>
```
Restart-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8e7fc-106">S2</span><span class="sxs-lookup"><span data-stu-id="8e7fc-106">S2</span></span>
```
Restart-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e7fc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8e7fc-107">DESCRIPTION</span></span>
<span data-ttu-id="8e7fc-108">Polecenie cmdlet **restart-AzureRmWebApp** zostanie zatrzymane, a następnie zostanie uruchomiona aplikacja Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="8e7fc-108">The **Restart-AzureRmWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="8e7fc-109">Jeśli aplikacja sieci Web jest zatrzymana, użyj polecenia cmdlet Start-AzureRmWebApp.</span><span class="sxs-lookup"><span data-stu-id="8e7fc-109">If the Web App is in a stopped state, use the Start-AzureRmWebApp cmdlet.</span></span>

## <span data-ttu-id="8e7fc-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8e7fc-110">EXAMPLES</span></span>

### <span data-ttu-id="8e7fc-111">Przykład 1: ponowne uruchamianie aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="8e7fc-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="8e7fc-112">To polecenie zatrzymuje aplikację Azure Web App o nazwie ContosoSite, która należy do grupy zasobów o nazwie Default-Web-Zachodnia, a następnie ponownie ją uruchamia.</span><span class="sxs-lookup"><span data-stu-id="8e7fc-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="8e7fc-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8e7fc-113">PARAMETERS</span></span>

### <span data-ttu-id="8e7fc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e7fc-114">-DefaultProfile</span></span>
<span data-ttu-id="8e7fc-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8e7fc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e7fc-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8e7fc-116">-Name</span></span>
<span data-ttu-id="8e7fc-117">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="8e7fc-117">WebApp Name</span></span>

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

### <span data-ttu-id="8e7fc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e7fc-118">-ResourceGroupName</span></span>
<span data-ttu-id="8e7fc-119">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8e7fc-119">Resource Group Name</span></span>

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

### <span data-ttu-id="8e7fc-120">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="8e7fc-120">-WebApp</span></span>
<span data-ttu-id="8e7fc-121">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="8e7fc-121">WebApp Object</span></span>

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

### <span data-ttu-id="8e7fc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e7fc-122">CommonParameters</span></span>
<span data-ttu-id="8e7fc-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e7fc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e7fc-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e7fc-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e7fc-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e7fc-125">INPUTS</span></span>

### <span data-ttu-id="8e7fc-126">Klienta</span><span class="sxs-lookup"><span data-stu-id="8e7fc-126">Site</span></span>
<span data-ttu-id="8e7fc-127">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="8e7fc-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="8e7fc-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8e7fc-128">OUTPUTS</span></span>

## <span data-ttu-id="8e7fc-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8e7fc-129">NOTES</span></span>

## <span data-ttu-id="8e7fc-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8e7fc-130">RELATED LINKS</span></span>

[<span data-ttu-id="8e7fc-131">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="8e7fc-131">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="8e7fc-132">Nowe — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="8e7fc-132">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="8e7fc-133">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="8e7fc-133">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="8e7fc-134">Start — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="8e7fc-134">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="8e7fc-135">Zatrzymaj — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="8e7fc-135">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


