---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
ms.openlocfilehash: 74c518d4713c19c7a1bb7b7d0b3341e164e22c35
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222097"
---
# <span data-ttu-id="17c60-101">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="17c60-101">Get-AzDeletedWebApp</span></span>

## <span data-ttu-id="17c60-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="17c60-102">SYNOPSIS</span></span>
<span data-ttu-id="17c60-103">Pobiera usunięte aplikacje sieci Web w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="17c60-103">Gets deleted web apps in the subscription.</span></span>

## <span data-ttu-id="17c60-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="17c60-104">SYNTAX</span></span>

```
Get-AzDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17c60-105">Opis</span><span class="sxs-lookup"><span data-stu-id="17c60-105">DESCRIPTION</span></span>
<span data-ttu-id="17c60-106">Polecenie cmdlet **Get-AzDeletedWebApp** zwraca wszystkie usunięte aplikacje sieci Web w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="17c60-106">The **Get-AzDeletedWebApp** cmdlet returns all deleted web apps in the subscription.</span></span> <span data-ttu-id="17c60-107">Usunięte aplikacje można opcjonalnie filtrować według grup zasobów, nazw i gniazd.</span><span class="sxs-lookup"><span data-stu-id="17c60-107">Deleted apps can optionally be filtered by resource group, name, and slot.</span></span> <span data-ttu-id="17c60-108">Może istnieć więcej niż jedna usunięta aplikacja z tą samą nazwą i grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="17c60-108">There can be more than one deleted app with the same name and resource group.</span></span> <span data-ttu-id="17c60-109">Zaznacz DeletionTime, aby rozróżnić usunięte aplikacje, które mają taką samą nazwę.</span><span class="sxs-lookup"><span data-stu-id="17c60-109">Check the DeletionTime to distinguish deleted apps that share the same name.</span></span>

## <span data-ttu-id="17c60-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="17c60-110">EXAMPLES</span></span>

### <span data-ttu-id="17c60-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="17c60-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="17c60-112">To polecenie pobiera usunięte aplikacje o nazwie ContosoSite należące do grupy zasobów Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="17c60-112">This command gets the deleted apps named ContosoSite belonging to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="17c60-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="17c60-113">PARAMETERS</span></span>

### <span data-ttu-id="17c60-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17c60-114">-DefaultProfile</span></span>
<span data-ttu-id="17c60-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="17c60-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17c60-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="17c60-116">-Location</span></span>
<span data-ttu-id="17c60-117">Lokalizacja usuniętej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="17c60-117">The location of the deleted app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17c60-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="17c60-118">-Name</span></span>
<span data-ttu-id="17c60-119">Nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="17c60-119">The name of the web app.</span></span>

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

### <span data-ttu-id="17c60-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17c60-120">-ResourceGroupName</span></span>
<span data-ttu-id="17c60-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="17c60-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="17c60-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="17c60-122">-Slot</span></span>
<span data-ttu-id="17c60-123">Nazwa miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="17c60-123">The name of the web app slot.</span></span>

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

### <span data-ttu-id="17c60-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17c60-124">CommonParameters</span></span>
<span data-ttu-id="17c60-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17c60-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17c60-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17c60-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17c60-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17c60-127">INPUTS</span></span>

### <span data-ttu-id="17c60-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="17c60-128">None</span></span>

## <span data-ttu-id="17c60-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="17c60-129">OUTPUTS</span></span>

### <span data-ttu-id="17c60-130">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. webapps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="17c60-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="17c60-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="17c60-131">NOTES</span></span>

## <span data-ttu-id="17c60-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="17c60-132">RELATED LINKS</span></span>

[<span data-ttu-id="17c60-133">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="17c60-133">Restore-AzDeletedWebApp</span></span>](./Restore-AzDeletedWebApp.md)