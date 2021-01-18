---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/new-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationService.md
ms.openlocfilehash: 821590b158478c38e5d4e997254e98a802d4befd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504170"
---
# <span data-ttu-id="995ce-101">New-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="995ce-101">New-AzCommunicationService</span></span>

## <span data-ttu-id="995ce-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="995ce-102">SYNOPSIS</span></span>
<span data-ttu-id="995ce-103">Utwórz nowe CommunicationService lub zaktualizuj istniejące CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="995ce-103">Create a new CommunicationService or update an existing CommunicationService.</span></span>

## <span data-ttu-id="995ce-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="995ce-104">SYNTAX</span></span>

```
New-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DataLocation <String>] [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="995ce-105">Opis</span><span class="sxs-lookup"><span data-stu-id="995ce-105">DESCRIPTION</span></span>
<span data-ttu-id="995ce-106">Utwórz nowe CommunicationService lub zaktualizuj istniejące CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="995ce-106">Create a new CommunicationService or update an existing CommunicationService.</span></span>

## <span data-ttu-id="995ce-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="995ce-107">EXAMPLES</span></span>

### <span data-ttu-id="995ce-108">Przykład 1. Tworzenie zasobu ACS</span><span class="sxs-lookup"><span data-stu-id="995ce-108">Example 1: Create a ACS resource</span></span>
```powershell
PS C:\> New-AzCommunicationService -ResourceGroupName ContosoResourceProvider1 -Name ContosoAcsResource1 -DataLocation UnitedStates -Location Global

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="995ce-109">Tworzy zasób ACS przy użyciu określonych parametrów.</span><span class="sxs-lookup"><span data-stu-id="995ce-109">Creates a ACS resource using the specified parameters.</span></span>

## <span data-ttu-id="995ce-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="995ce-110">PARAMETERS</span></span>

### <span data-ttu-id="995ce-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="995ce-111">-AsJob</span></span>
<span data-ttu-id="995ce-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="995ce-112">Run the command as a job</span></span>

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

### <span data-ttu-id="995ce-113">-Lokalizacja datalocation</span><span class="sxs-lookup"><span data-stu-id="995ce-113">-DataLocation</span></span>
<span data-ttu-id="995ce-114">Miejsce, w którym usługa komunikacyjna przechowuje swoje dane w stanie spoczynku.</span><span class="sxs-lookup"><span data-stu-id="995ce-114">The location where the communication service stores its data at rest.</span></span>

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

### <span data-ttu-id="995ce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="995ce-115">-DefaultProfile</span></span>
<span data-ttu-id="995ce-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="995ce-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="995ce-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="995ce-117">-Location</span></span>
<span data-ttu-id="995ce-118">Lokalizacja platformy Azure, w której jest uruchomiony CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="995ce-118">The Azure location where the CommunicationService is running.</span></span>

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

### <span data-ttu-id="995ce-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="995ce-119">-Name</span></span>
<span data-ttu-id="995ce-120">Nazwa zasobu CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="995ce-120">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="995ce-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="995ce-121">-NoWait</span></span>
<span data-ttu-id="995ce-122">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="995ce-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="995ce-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="995ce-123">-ResourceGroupName</span></span>
<span data-ttu-id="995ce-124">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="995ce-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="995ce-125">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="995ce-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="995ce-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="995ce-126">-SubscriptionId</span></span>
<span data-ttu-id="995ce-127">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="995ce-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="995ce-128">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="995ce-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="995ce-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="995ce-129">-Tag</span></span>
<span data-ttu-id="995ce-130">Tagi usługi, która jest listą par wartości klucza opisujących zasób.</span><span class="sxs-lookup"><span data-stu-id="995ce-130">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="995ce-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="995ce-131">-Confirm</span></span>
<span data-ttu-id="995ce-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="995ce-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="995ce-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="995ce-133">-WhatIf</span></span>
<span data-ttu-id="995ce-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="995ce-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="995ce-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="995ce-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="995ce-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="995ce-136">CommonParameters</span></span>
<span data-ttu-id="995ce-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="995ce-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="995ce-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="995ce-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="995ce-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="995ce-139">INPUTS</span></span>

## <span data-ttu-id="995ce-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="995ce-140">OUTPUTS</span></span>

### <span data-ttu-id="995ce-141">Microsoft. Azure. PowerShell. cmdlet. Communication. models. Api20200820Preview. ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="995ce-141">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="995ce-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="995ce-142">NOTES</span></span>

<span data-ttu-id="995ce-143">PISUJE</span><span class="sxs-lookup"><span data-stu-id="995ce-143">ALIASES</span></span>

## <span data-ttu-id="995ce-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="995ce-144">RELATED LINKS</span></span>

