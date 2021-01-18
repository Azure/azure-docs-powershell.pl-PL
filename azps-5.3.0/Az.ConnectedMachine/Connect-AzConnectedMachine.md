---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/connect-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
ms.openlocfilehash: 281d456eb7612914bac546b3d361238bb5056626
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501817"
---
# <span data-ttu-id="041bb-101">Connect-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="041bb-101">Connect-AzConnectedMachine</span></span>

## <span data-ttu-id="041bb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="041bb-102">SYNOPSIS</span></span>
<span data-ttu-id="041bb-103">Interfejs API umożliwiający zarejestrowanie nowego komputera, a w związku z tym utworzenie prześledzonego zasobu w ARM</span><span class="sxs-lookup"><span data-stu-id="041bb-103">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="041bb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="041bb-104">SYNTAX</span></span>

```
Connect-AzConnectedMachine [-ResourceGroupName] <String> [-Location] <String> [[-SubscriptionId] <String>]
 [[-Name] <String>] [[-DefaultProfile] <PSObject>] [[-PSSession] <PSSession[]>] [[-Tag] <Hashtable>]
 [[-Proxy] <Uri>] [<CommonParameters>]
```

## <span data-ttu-id="041bb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="041bb-105">DESCRIPTION</span></span>
<span data-ttu-id="041bb-106">Interfejs API umożliwiający zarejestrowanie nowego komputera, a w związku z tym utworzenie prześledzonego zasobu w ARM</span><span class="sxs-lookup"><span data-stu-id="041bb-106">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="041bb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="041bb-107">EXAMPLES</span></span>

### <span data-ttu-id="041bb-108">Przykład 1: znajduje się na pokładzie komputera, który jest podłączony do komputera.</span><span class="sxs-lookup"><span data-stu-id="041bb-108">Example 1: Onboards the machine you're on as a connected machine</span></span>
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

<span data-ttu-id="041bb-109">Znajduje się na płycie, na którym znajduje się komputer, na którym jesteś podłączony.</span><span class="sxs-lookup"><span data-stu-id="041bb-109">Onboards the machine you're on as a connected machine.</span></span>

### <span data-ttu-id="041bb-110">Przykład 2: komputer zdalny jest podłączony do podłączonego urządzenia</span><span class="sxs-lookup"><span data-stu-id="041bb-110">Example 2: Onboards a remote machine as a connected device</span></span>
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

<span data-ttu-id="041bb-111">Na komputerze zdalnym jako urządzenie podłączone za pomocą funkcji komunikacji zdalnej programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="041bb-111">Onboards a remote machine as a connected device using PowerShell remoting.</span></span>
<span data-ttu-id="041bb-112">Uwaga: obecnie jest obsługiwany tylko system Windows jako element docelowy.</span><span class="sxs-lookup"><span data-stu-id="041bb-112">Note: only Windows as the target is supported at this time.</span></span>

## <span data-ttu-id="041bb-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="041bb-113">PARAMETERS</span></span>

### <span data-ttu-id="041bb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="041bb-114">-DefaultProfile</span></span>
<span data-ttu-id="041bb-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="041bb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="041bb-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="041bb-116">-Location</span></span>
<span data-ttu-id="041bb-117">Lokalizacja utworzonego ConnectedMachine.</span><span class="sxs-lookup"><span data-stu-id="041bb-117">The location for the created ConnectedMachine.</span></span>

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

### <span data-ttu-id="041bb-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="041bb-118">-Name</span></span>
<span data-ttu-id="041bb-119">Nazwa, która będzie używana dla tego komputera.</span><span class="sxs-lookup"><span data-stu-id="041bb-119">The name that will be used for this machine.</span></span>
<span data-ttu-id="041bb-120">Nazwa hosta jest używana domyślnie.</span><span class="sxs-lookup"><span data-stu-id="041bb-120">The hostname is used by default.</span></span>

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

### <span data-ttu-id="041bb-121">-Proxy</span><span class="sxs-lookup"><span data-stu-id="041bb-121">-Proxy</span></span>
<span data-ttu-id="041bb-122">Identyfikator URI serwera proxy, który ma być używany</span><span class="sxs-lookup"><span data-stu-id="041bb-122">The URI for the proxy server to use</span></span>

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

### <span data-ttu-id="041bb-123">-PSSession</span><span class="sxs-lookup"><span data-stu-id="041bb-123">-PSSession</span></span>
<span data-ttu-id="041bb-124">Po wybraniu tej polecenia narzędzie, które dołączają do komputerów platformy Azure, będzie uruchamiane w ramach każdego PSSession.</span><span class="sxs-lookup"><span data-stu-id="041bb-124">When specified, the command that onboards machines to Azure will be run within each PSSession.</span></span>
<span data-ttu-id="041bb-125">Uwaga: Ta funkcja działa tylko w systemie Windows.</span><span class="sxs-lookup"><span data-stu-id="041bb-125">NOTE: This only works on Windows for now.</span></span>

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

### <span data-ttu-id="041bb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="041bb-126">-ResourceGroupName</span></span>
<span data-ttu-id="041bb-127">Nazwa grupy zasobów, do której chcesz dodać maszynę.</span><span class="sxs-lookup"><span data-stu-id="041bb-127">The name of the resource group you want to add the machine to.</span></span>

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

### <span data-ttu-id="041bb-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="041bb-128">-SubscriptionId</span></span>
<span data-ttu-id="041bb-129">Identyfikator subskrypcji, do której chcesz dodać maszynę.</span><span class="sxs-lookup"><span data-stu-id="041bb-129">The ID of the subscription you want to add the machine to.</span></span>

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

### <span data-ttu-id="041bb-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="041bb-130">-Tag</span></span>
<span data-ttu-id="041bb-131">Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="041bb-131">Resource tags.</span></span>

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

### <span data-ttu-id="041bb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="041bb-132">CommonParameters</span></span>
<span data-ttu-id="041bb-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="041bb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="041bb-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="041bb-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="041bb-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="041bb-135">INPUTS</span></span>

## <span data-ttu-id="041bb-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="041bb-136">OUTPUTS</span></span>

## <span data-ttu-id="041bb-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="041bb-137">NOTES</span></span>

<span data-ttu-id="041bb-138">PISUJE</span><span class="sxs-lookup"><span data-stu-id="041bb-138">ALIASES</span></span>

## <span data-ttu-id="041bb-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="041bb-139">RELATED LINKS</span></span>

