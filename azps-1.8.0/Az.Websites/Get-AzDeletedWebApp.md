---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
ms.openlocfilehash: fabbaf6e34a39767c9ca0acdadd3fdc05d8e260f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707334"
---
# <span data-ttu-id="1b4fc-101">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="1b4fc-101">Get-AzDeletedWebApp</span></span>

## <span data-ttu-id="1b4fc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1b4fc-102">SYNOPSIS</span></span>
<span data-ttu-id="1b4fc-103">Pobiera usunięte aplikacje sieci Web w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1b4fc-103">Gets deleted web apps in the subscription.</span></span>

## <span data-ttu-id="1b4fc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1b4fc-104">SYNTAX</span></span>

```
Get-AzDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b4fc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1b4fc-105">DESCRIPTION</span></span>
<span data-ttu-id="1b4fc-106">Polecenie cmdlet **Get-AzDeletedWebApp** zwraca wszystkie usunięte aplikacje sieci Web w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1b4fc-106">The **Get-AzDeletedWebApp** cmdlet returns all deleted web apps in the subscription.</span></span> <span data-ttu-id="1b4fc-107">Usunięte aplikacje można opcjonalnie filtrować według grup zasobów, nazw i gniazd.</span><span class="sxs-lookup"><span data-stu-id="1b4fc-107">Deleted apps can optionally be filtered by resource group, name, and slot.</span></span> <span data-ttu-id="1b4fc-108">Może istnieć więcej niż jedna usunięta aplikacja z tą samą nazwą i grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="1b4fc-108">There can be more than one deleted app with the same name and resource group.</span></span> <span data-ttu-id="1b4fc-109">Zaznacz DeletionTime, aby rozróżnić usunięte aplikacje, które mają taką samą nazwę.</span><span class="sxs-lookup"><span data-stu-id="1b4fc-109">Check the DeletionTime to distinguish deleted apps that share the same name.</span></span>

## <span data-ttu-id="1b4fc-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1b4fc-110">EXAMPLES</span></span>

### <span data-ttu-id="1b4fc-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1b4fc-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="1b4fc-112">To polecenie pobiera usunięte aplikacje o nazwie ContosoSite należące do grupy zasobów Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="1b4fc-112">This command gets the deleted apps named ContosoSite belonging to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="1b4fc-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1b4fc-113">PARAMETERS</span></span>

### <span data-ttu-id="1b4fc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b4fc-114">-DefaultProfile</span></span>
<span data-ttu-id="1b4fc-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1b4fc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b4fc-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1b4fc-116">-Name</span></span>
<span data-ttu-id="1b4fc-117">Nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="1b4fc-117">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b4fc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b4fc-118">-ResourceGroupName</span></span>
<span data-ttu-id="1b4fc-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1b4fc-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b4fc-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="1b4fc-120">-Slot</span></span>
<span data-ttu-id="1b4fc-121">Nazwa miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="1b4fc-121">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b4fc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b4fc-122">CommonParameters</span></span>
<span data-ttu-id="1b4fc-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b4fc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b4fc-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b4fc-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b4fc-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b4fc-125">INPUTS</span></span>

### <span data-ttu-id="1b4fc-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1b4fc-126">None</span></span>

## <span data-ttu-id="1b4fc-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1b4fc-127">OUTPUTS</span></span>

### <span data-ttu-id="1b4fc-128">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. webapps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="1b4fc-128">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="1b4fc-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1b4fc-129">NOTES</span></span>

## <span data-ttu-id="1b4fc-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1b4fc-130">RELATED LINKS</span></span>

[<span data-ttu-id="1b4fc-131">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="1b4fc-131">Restore-AzDeletedWebApp</span></span>](./Restore-AzDeletedWebApp.md)