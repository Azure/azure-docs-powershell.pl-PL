---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmDeletedWebApp.md
ms.openlocfilehash: 75ad4e1fabb511ee4ca3cff024389a8e826aeadd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546336"
---
# <span data-ttu-id="d95e8-101">Get-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="d95e8-101">Get-AzureRmDeletedWebApp</span></span>

## <span data-ttu-id="d95e8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d95e8-102">SYNOPSIS</span></span>
<span data-ttu-id="d95e8-103">Pobiera usunięte aplikacje sieci Web w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d95e8-103">Gets deleted web apps in the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d95e8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d95e8-104">SYNTAX</span></span>

```
Get-AzureRmDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d95e8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d95e8-105">DESCRIPTION</span></span>
<span data-ttu-id="d95e8-106">Polecenie cmdlet **Get-AzureRmDeletedWebApp** zwraca wszystkie usunięte aplikacje sieci Web w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d95e8-106">The **Get-AzureRmDeletedWebApp** cmdlet returns all deleted web apps in the subscription.</span></span> <span data-ttu-id="d95e8-107">Usunięte aplikacje można opcjonalnie filtrować według grup zasobów, nazw i gniazd.</span><span class="sxs-lookup"><span data-stu-id="d95e8-107">Deleted apps can optionally be filtered by resource group, name, and slot.</span></span> <span data-ttu-id="d95e8-108">Może istnieć więcej niż jedna usunięta aplikacja z tą samą nazwą i grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="d95e8-108">There can be more than one deleted app with the same name and resource group.</span></span> <span data-ttu-id="d95e8-109">Zaznacz DeletionTime, aby rozróżnić usunięte aplikacje, które mają taką samą nazwę.</span><span class="sxs-lookup"><span data-stu-id="d95e8-109">Check the DeletionTime to distinguish deleted apps that share the same name.</span></span>

## <span data-ttu-id="d95e8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d95e8-110">EXAMPLES</span></span>

### <span data-ttu-id="d95e8-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d95e8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="d95e8-112">To polecenie pobiera usunięte aplikacje o nazwie ContosoSite należące do grupy zasobów Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="d95e8-112">This command gets the deleted apps named ContosoSite belonging to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="d95e8-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d95e8-113">PARAMETERS</span></span>

### <span data-ttu-id="d95e8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d95e8-114">-DefaultProfile</span></span>
<span data-ttu-id="d95e8-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d95e8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d95e8-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d95e8-116">-Name</span></span>
<span data-ttu-id="d95e8-117">Nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="d95e8-117">The name of the web app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d95e8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d95e8-118">-ResourceGroupName</span></span>
<span data-ttu-id="d95e8-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d95e8-119">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d95e8-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="d95e8-120">-Slot</span></span>
<span data-ttu-id="d95e8-121">Nazwa miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="d95e8-121">The name of the web app slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d95e8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d95e8-122">CommonParameters</span></span>
<span data-ttu-id="d95e8-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d95e8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d95e8-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d95e8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d95e8-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d95e8-125">INPUTS</span></span>

### <span data-ttu-id="d95e8-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d95e8-126">None</span></span>

## <span data-ttu-id="d95e8-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d95e8-127">OUTPUTS</span></span>

### <span data-ttu-id="d95e8-128">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. webapps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="d95e8-128">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="d95e8-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d95e8-129">NOTES</span></span>

## <span data-ttu-id="d95e8-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d95e8-130">RELATED LINKS</span></span>

[<span data-ttu-id="d95e8-131">Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="d95e8-131">Restore-AzureRmDeletedWebApp</span></span>](./Restore-AzureRmDeletedWebApp.md)
