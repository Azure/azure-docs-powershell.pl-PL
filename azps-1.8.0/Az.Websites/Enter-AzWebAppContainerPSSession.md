---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/enter-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
ms.openlocfilehash: b18008268ffd07369cf527c53d6ad693a38d85f1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707343"
---
# <span data-ttu-id="01225-101">Enter-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="01225-101">Enter-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="01225-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="01225-102">SYNOPSIS</span></span>
<span data-ttu-id="01225-103">Otwiera zdalną sesję programu PowerShell w kontenerze systemu Windows określonym w danej witrynie lub gnieździe i danej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="01225-103">Opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="01225-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="01225-104">SYNTAX</span></span>

### <span data-ttu-id="01225-105">S1 (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="01225-105">S1 (Default)</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01225-106">S2</span><span class="sxs-lookup"><span data-stu-id="01225-106">S2</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01225-107">Opis</span><span class="sxs-lookup"><span data-stu-id="01225-107">DESCRIPTION</span></span>
<span data-ttu-id="01225-108">otwiera zdalną sesję programu PowerShell w kontenerze systemu Windows określonym w danej witrynie lub gnieździe i danej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="01225-108">opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="01225-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="01225-109">EXAMPLES</span></span>

### <span data-ttu-id="01225-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="01225-110">Example 1</span></span>
```
PS C:\> Enter-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="01225-111">To polecenie otwiera zdalną sesję programu PowerShell w aplikacji kontenerowej systemu Windows ContosoASP</span><span class="sxs-lookup"><span data-stu-id="01225-111">This command opens a remote PowerShell session into the windows container app ContosoASP</span></span>

## <span data-ttu-id="01225-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="01225-112">PARAMETERS</span></span>

### <span data-ttu-id="01225-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01225-113">-DefaultProfile</span></span>
<span data-ttu-id="01225-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="01225-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01225-115">-Force</span><span class="sxs-lookup"><span data-stu-id="01225-115">-Force</span></span>
<span data-ttu-id="01225-116">Tworzenie sesji programu PowerShell bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="01225-116">Create the PowerShell session without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01225-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="01225-117">-Name</span></span>
<span data-ttu-id="01225-118">Nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="01225-118">The name of the web app.</span></span>

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

### <span data-ttu-id="01225-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01225-119">-PassThru</span></span>
<span data-ttu-id="01225-120">Zwracanie wartości oznaczającej sukces lub niepowodzenie</span><span class="sxs-lookup"><span data-stu-id="01225-120">Return a value indicating success or failure</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01225-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01225-121">-ResourceGroupName</span></span>
<span data-ttu-id="01225-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="01225-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="01225-123">-Slotname</span><span class="sxs-lookup"><span data-stu-id="01225-123">-SlotName</span></span>
<span data-ttu-id="01225-124">Nazwa miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="01225-124">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01225-125">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="01225-125">-WebApp</span></span>
<span data-ttu-id="01225-126">Obiekt aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="01225-126">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01225-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="01225-127">-Confirm</span></span>
<span data-ttu-id="01225-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01225-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01225-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01225-129">-WhatIf</span></span>
<span data-ttu-id="01225-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01225-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="01225-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="01225-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01225-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01225-132">CommonParameters</span></span>
<span data-ttu-id="01225-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01225-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01225-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01225-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01225-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01225-135">INPUTS</span></span>

### <span data-ttu-id="01225-136">System. String</span><span class="sxs-lookup"><span data-stu-id="01225-136">System.String</span></span>

### <span data-ttu-id="01225-137">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="01225-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="01225-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="01225-138">OUTPUTS</span></span>

### <span data-ttu-id="01225-139">System. void</span><span class="sxs-lookup"><span data-stu-id="01225-139">System.Void</span></span>

## <span data-ttu-id="01225-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="01225-140">NOTES</span></span>

## <span data-ttu-id="01225-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="01225-141">RELATED LINKS</span></span>
