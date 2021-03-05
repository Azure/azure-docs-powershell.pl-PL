---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/connect-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
ms.openlocfilehash: b0e52f6d163579e1d481f841d3a58e8b15c6658b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012426"
---
# <span data-ttu-id="f809b-101">Connect-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="f809b-101">Connect-AzConnectedMachine</span></span>

## <span data-ttu-id="f809b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f809b-102">SYNOPSIS</span></span>
<span data-ttu-id="f809b-103">Interfejs API do rejestrowania nowego komputera, a tym samym tworzenia śledzonego zasobu w ARM</span><span class="sxs-lookup"><span data-stu-id="f809b-103">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="f809b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f809b-104">SYNTAX</span></span>

```
Connect-AzConnectedMachine [-ResourceGroupName] <String> [-Location] <String> [[-SubscriptionId] <String>]
 [[-Name] <String>] [[-DefaultProfile] <PSObject>] [[-PSSession] <PSSession[]>] [[-Tag] <Hashtable>]
 [[-Proxy] <Uri>] [<CommonParameters>]
```

## <span data-ttu-id="f809b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f809b-105">DESCRIPTION</span></span>
<span data-ttu-id="f809b-106">Interfejs API do rejestrowania nowego komputera, a tym samym tworzenia śledzonego zasobu w ARM</span><span class="sxs-lookup"><span data-stu-id="f809b-106">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="f809b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f809b-107">EXAMPLES</span></span>

### <span data-ttu-id="f809b-108">Przykład 1. Dołącza komputer, na których jesteś, jako połączony komputer</span><span class="sxs-lookup"><span data-stu-id="f809b-108">Example 1: Onboards the machine you're on as a connected machine</span></span>
```powershell
PS C:\> Connect-AzConnectedMachine -ResourceGroupName contoso-connected-machines -Name linux_eastus1_1 -Location eastus

< truncated output of installing the azcmagent >

time="2020-08-07T13:13:25-07:00" level=info msg="Onboarding Machine. It usually takes a few minutes to complete. Sometimes it may take longer depending on network and server load status."
time="2020-08-07T13:13:25-07:00" level=info msg="Check network connectivity to all endpoints..."
time="2020-08-07T13:13:29-07:00" level=info msg="All endpoints are available... continue onboarding"
time="2020-08-07T13:13:50-07:00" level=info msg="Successfully Onboarded Resource to Azure" VM Id=978ab182-6cf0-4de3-a58b-53c8d0a3235e

Name             Location OSName   Status     ProvisioningState
----             -------- ------   ------     -----------------
linux_eastus1_1  eastus   linux    Connected  Succeeded
```

<span data-ttu-id="f809b-109">Dołącza komputer, na których jesteś, jako połączony komputer.</span><span class="sxs-lookup"><span data-stu-id="f809b-109">Onboards the machine you're on as a connected machine.</span></span>

### <span data-ttu-id="f809b-110">Przykład 2. Dołącza komputer zdalny jako podłączone urządzenie</span><span class="sxs-lookup"><span data-stu-id="f809b-110">Example 2: Onboards a remote machine as a connected device</span></span>
```powershell
PS C:\> $session = Connect-PSSession -ComputerName WINBOX
PS C:\> Connect-AzConnectedMachine -ResourceGroupName contoso-rg -Name win_eastus1_1 -Location eastus -PSSession $session

< truncated output of installing the azcmagent >

time="2020-08-07T13:13:25-07:00" level=info msg="Onboarding Machine. It usually takes a few minutes to complete. Sometimes it may take longer depending on network and server load status."
time="2020-08-07T13:13:25-07:00" level=info msg="Check network connectivity to all endpoints..."
time="2020-08-07T13:13:29-07:00" level=info msg="All endpoints are available... continue onboarding"
time="2020-08-07T13:13:50-07:00" level=info msg="Successfully Onboarded Resource to Azure" VM Id=978ab182-6cf0-4de3-a58b-53c8d0a3236a

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
win_eastus1_1  eastus   windows  Connected  Succeeded
```

<span data-ttu-id="f809b-111">Dołącza komputer zdalny jako połączone urządzenie przy użyciu ponownego odsłuchiania programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f809b-111">Onboards a remote machine as a connected device using PowerShell remoting.</span></span>
<span data-ttu-id="f809b-112">Uwaga: w tej chwili obsługiwany jest tylko system Windows jako element docelowy.</span><span class="sxs-lookup"><span data-stu-id="f809b-112">Note: only Windows as the target is supported at this time.</span></span>

## <span data-ttu-id="f809b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f809b-113">PARAMETERS</span></span>

### <span data-ttu-id="f809b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f809b-114">-DefaultProfile</span></span>
<span data-ttu-id="f809b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f809b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f809b-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f809b-116">-Location</span></span>
<span data-ttu-id="f809b-117">Lokalizacja utworzonego użytkownika ConnectedMachine.</span><span class="sxs-lookup"><span data-stu-id="f809b-117">The location for the created ConnectedMachine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f809b-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f809b-118">-Name</span></span>
<span data-ttu-id="f809b-119">Nazwa, która będzie używana dla tego komputera.</span><span class="sxs-lookup"><span data-stu-id="f809b-119">The name that will be used for this machine.</span></span>
<span data-ttu-id="f809b-120">Nazwa hosta jest używana domyślnie.</span><span class="sxs-lookup"><span data-stu-id="f809b-120">The hostname is used by default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f809b-121">— serwer proxy</span><span class="sxs-lookup"><span data-stu-id="f809b-121">-Proxy</span></span>
<span data-ttu-id="f809b-122">Adres URI serwera proxy do użycia</span><span class="sxs-lookup"><span data-stu-id="f809b-122">The URI for the proxy server to use</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f809b-123">-PSSession</span><span class="sxs-lookup"><span data-stu-id="f809b-123">-PSSession</span></span>
<span data-ttu-id="f809b-124">W określonym przypadku polecenie, które uruchamia komputery na platformie Azure, będzie uruchamiane w ramach każdego polecenia PSSession.</span><span class="sxs-lookup"><span data-stu-id="f809b-124">When specified, the command that onboards machines to Azure will be run within each PSSession.</span></span>
<span data-ttu-id="f809b-125">UWAGA: Ta funkcja na razie działa tylko w systemie Windows.</span><span class="sxs-lookup"><span data-stu-id="f809b-125">NOTE: This only works on Windows for now.</span></span>

```yaml
Type: System.Management.Automation.Runspaces.PSSession[]
Parameter Sets: (All)
Aliases: Session

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f809b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f809b-126">-ResourceGroupName</span></span>
<span data-ttu-id="f809b-127">Nazwa grupy zasobów, do której chcesz dodać komputer.</span><span class="sxs-lookup"><span data-stu-id="f809b-127">The name of the resource group you want to add the machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f809b-128">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f809b-128">-SubscriptionId</span></span>
<span data-ttu-id="f809b-129">Identyfikator subskrypcji, do której chcesz dodać komputer.</span><span class="sxs-lookup"><span data-stu-id="f809b-129">The ID of the subscription you want to add the machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f809b-130">— Tag</span><span class="sxs-lookup"><span data-stu-id="f809b-130">-Tag</span></span>
<span data-ttu-id="f809b-131">Tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="f809b-131">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f809b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f809b-132">CommonParameters</span></span>
<span data-ttu-id="f809b-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f809b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f809b-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f809b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f809b-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f809b-135">INPUTS</span></span>

## <span data-ttu-id="f809b-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f809b-136">OUTPUTS</span></span>

## <span data-ttu-id="f809b-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f809b-137">NOTES</span></span>

<span data-ttu-id="f809b-138">ALIASY</span><span class="sxs-lookup"><span data-stu-id="f809b-138">ALIASES</span></span>

## <span data-ttu-id="f809b-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f809b-139">RELATED LINKS</span></span>

