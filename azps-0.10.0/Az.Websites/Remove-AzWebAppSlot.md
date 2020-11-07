---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/remove-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebAppSlot.md
ms.openlocfilehash: 04813b04d3d2499de549655edb6398550ce25536
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891869"
---
# <span data-ttu-id="c131b-101">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c131b-101">Remove-AzWebAppSlot</span></span>

## <span data-ttu-id="c131b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c131b-102">SYNOPSIS</span></span>

## <span data-ttu-id="c131b-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c131b-103">SYNTAX</span></span>

### <span data-ttu-id="c131b-104">S1</span><span class="sxs-lookup"><span data-stu-id="c131b-104">S1</span></span>
```
Remove-AzWebAppSlot [-Force] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c131b-105">S2</span><span class="sxs-lookup"><span data-stu-id="c131b-105">S2</span></span>
```
Remove-AzWebAppSlot [-Force] [-WebApp] <Site> [-AsJob][-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c131b-106">Opis</span><span class="sxs-lookup"><span data-stu-id="c131b-106">DESCRIPTION</span></span>
<span data-ttu-id="c131b-107">Polecenie cmdlet **Remove-AzWebAppSlot** usuwa miejsce w usłudze Azure Web App, pod warunkiem, że grupa zasobów i nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="c131b-107">The **Remove-AzWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="c131b-108">To polecenie cmdlet domyślnie usuwa także wszystkie gniazda i metryki.</span><span class="sxs-lookup"><span data-stu-id="c131b-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="c131b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c131b-109">EXAMPLES</span></span>

### <span data-ttu-id="c131b-110">Przykład 1. Usuń miejsce aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="c131b-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "ContosoSlot"
```

<span data-ttu-id="c131b-111">To polecenie powoduje usunięcie gniazda o nazwie Slot001 skojarzonego z aplikacją sieci Web ContosoSite należącej do grupy zasobów o nazwie Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="c131b-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="c131b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c131b-112">PARAMETERS</span></span>

### <span data-ttu-id="c131b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c131b-113">-DefaultProfile</span></span>
<span data-ttu-id="c131b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c131b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c131b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c131b-115">-Force</span></span>
<span data-ttu-id="c131b-116">Wymuszone usuwanie opcji</span><span class="sxs-lookup"><span data-stu-id="c131b-116">Forcefully Remove Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c131b-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c131b-117">-Name</span></span>
<span data-ttu-id="c131b-118">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="c131b-118">WebApp Name</span></span>

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

### <span data-ttu-id="c131b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c131b-119">-ResourceGroupName</span></span>
<span data-ttu-id="c131b-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c131b-120">Resource Group Name</span></span>

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

### <span data-ttu-id="c131b-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="c131b-121">-Slot</span></span>
<span data-ttu-id="c131b-122">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="c131b-122">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c131b-123">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="c131b-123">-WebApp</span></span>
<span data-ttu-id="c131b-124">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="c131b-124">WebApp Object</span></span>

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

### <span data-ttu-id="c131b-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c131b-125">-Confirm</span></span>
<span data-ttu-id="c131b-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c131b-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c131b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c131b-127">-WhatIf</span></span>
<span data-ttu-id="c131b-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c131b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c131b-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c131b-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="c131b-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c131b-130">-AsJob</span></span>
<span data-ttu-id="c131b-131">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c131b-131">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c131b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c131b-132">CommonParameters</span></span>
<span data-ttu-id="c131b-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c131b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c131b-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c131b-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c131b-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c131b-135">INPUTS</span></span>

### <span data-ttu-id="c131b-136">Klienta</span><span class="sxs-lookup"><span data-stu-id="c131b-136">Site</span></span>
<span data-ttu-id="c131b-137">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="c131b-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="c131b-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c131b-138">OUTPUTS</span></span>

### <span data-ttu-id="c131b-139">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c131b-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="c131b-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c131b-140">NOTES</span></span>

## <span data-ttu-id="c131b-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c131b-141">RELATED LINKS</span></span>

[<span data-ttu-id="c131b-142">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c131b-142">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="c131b-143">Nowe — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c131b-143">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="c131b-144">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c131b-144">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="c131b-145">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c131b-145">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="c131b-146">Start — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c131b-146">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="c131b-147">Zatrzymaj — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c131b-147">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="c131b-148">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c131b-148">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
