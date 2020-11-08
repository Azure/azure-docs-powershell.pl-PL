---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 2287E103-442D-47FB-8279-0AE5936412C9
online version: ''
schema: 2.0.0
ms.openlocfilehash: f6a12f0e74964e096577b5a4fec0a46fd41d7872
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055168"
---
# <span data-ttu-id="e8018-101">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e8018-101">New-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="e8018-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e8018-102">SYNOPSIS</span></span>
<span data-ttu-id="e8018-103">Tworzy profil w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="e8018-103">Creates a Traffic Manager profile.</span></span>

## <span data-ttu-id="e8018-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e8018-104">SYNTAX</span></span>

```
New-AzureTrafficManagerProfile -Name <String> -DomainName <String> -LoadBalancingMethod <String>
 -MonitorPort <Int32> -MonitorProtocol <String> -MonitorRelativePath <String> -Ttl <Int32>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e8018-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e8018-105">DESCRIPTION</span></span>
<span data-ttu-id="e8018-106">Polecenie cmdlet **New-AzureTrafficManagerProfile** tworzy profil usługi Microsoft Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="e8018-106">The **New-AzureTrafficManagerProfile** cmdlet creates a Microsoft Azure Traffic Manager profile.</span></span>

<span data-ttu-id="e8018-107">Po utworzeniu profilu, w którym *LoadBalancingMethod* wartość "awaryjna", możesz określić kolejność przejęcia awaryjnego punktów końcowych dodawanych do profilu za pomocą polecenia cmdlet Add-AzureTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e8018-107">After you create a profile where you set the *LoadBalancingMethod* value to "Failover", you can determine the failover order of the endpoints you add to your profile with the Add-AzureTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="e8018-108">Aby uzyskać więcej informacji, zobacz przykład 2 poniżej.</span><span class="sxs-lookup"><span data-stu-id="e8018-108">For more information, see Example 2 below.</span></span>

## <span data-ttu-id="e8018-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e8018-109">EXAMPLES</span></span>

### <span data-ttu-id="e8018-110">Przykład 1: Tworzenie profilu w usłudze Traffic Manager</span><span class="sxs-lookup"><span data-stu-id="e8018-110">Example 1: Create a Traffic Manager profile</span></span>
```
PS C:\>New-AzureTrafficManagerProfile -Name "MyProfile" -DomainName "My.profile.trafficmanager.net" -LoadBalancingMethod "RoundRobin" -Ttl 30 -MonitorProtocol "Http" -MonitorPort 80 -MonitorRelativePath "/"
```

<span data-ttu-id="e8018-111">To polecenie tworzy profil usługi Traffic Manager o nazwie Moja profil w określonej domenie Menedżera ruchu z metodą okrężną równoważenia obciążenia, czyli wartością TTL 30 sekund, protokołem monitorowania HTTP, monitorowaniem portu 80 i określoną ścieżką.</span><span class="sxs-lookup"><span data-stu-id="e8018-111">This command creates a Traffic Manager profile named MyProfile in the specified Traffic Manager domain with a Round Robin load balancing method, a TTL of 30 seconds, HTTP monitoring protocol, monitoring port 80, and with the specified path.</span></span>

### <span data-ttu-id="e8018-112">Przykład 2: Zmienianie kolejności punktów końcowych na pożądaną kolejność w trybie failover</span><span class="sxs-lookup"><span data-stu-id="e8018-112">Example 2: Reorder endpoints to desired failover order</span></span>
```
PS C:\>$Profile = Get-AzureTrafficManagerProfile -Name "MyProfile"
PS C:\> $Profile.Endpoints[0],$Profile.Endpoints[1] = $Profile.Endpoints[1],$Profile.Endpoints[0]
PS C:\> $Profile = Set-AzureTrafficManagerProfile
```

<span data-ttu-id="e8018-113">Ten przykład zmienia kolejność punktów końcowych dodanych do polecenia mój profil do wybranego zlecenia trybu failover.</span><span class="sxs-lookup"><span data-stu-id="e8018-113">This example reorders the endpoints added to MyProfile to the desired failover order.</span></span>

<span data-ttu-id="e8018-114">Pierwsze polecenie pobiera obiekt profilu usługi Traffic Manager o nazwie Moja profil i zapisuje obiekt w zmiennej $Profile.</span><span class="sxs-lookup"><span data-stu-id="e8018-114">The first command gets the Traffic Manager profile object named MyProfile and stores the object in the $Profile variable.</span></span>

<span data-ttu-id="e8018-115">Drugie polecenie ponownie porządkuje punkty końcowe z tablicy punktów końcowych do kolejności, w której ma się odbywać przejście.</span><span class="sxs-lookup"><span data-stu-id="e8018-115">The second command re-orders the endpoints from  the endpoints array to the order in which failover should occur.</span></span>

<span data-ttu-id="e8018-116">Ostatnie polecenie aktualizuje profil usługi Traffic Manager przechowywany w $Profile z nową kolejnością punktów końcowych.</span><span class="sxs-lookup"><span data-stu-id="e8018-116">The last command updates the Traffic Manager profile stored in $Profile with the new endpoint order.</span></span>

## <span data-ttu-id="e8018-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e8018-117">PARAMETERS</span></span>

### <span data-ttu-id="e8018-118">-NazwaDomeny</span><span class="sxs-lookup"><span data-stu-id="e8018-118">-DomainName</span></span>
<span data-ttu-id="e8018-119">Określa nazwę domeny profilu usługi Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="e8018-119">Specifies the domain name of the Traffic Manager profile.</span></span>
<span data-ttu-id="e8018-120">To musi być poddomeną trafficmanager.net.</span><span class="sxs-lookup"><span data-stu-id="e8018-120">This must be a subdomain of trafficmanager.net.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8018-121">-LoadBalancingMethod</span><span class="sxs-lookup"><span data-stu-id="e8018-121">-LoadBalancingMethod</span></span>
<span data-ttu-id="e8018-122">Określa metodę równoważenia obciążenia używaną do rozpowszechniania połączenia.</span><span class="sxs-lookup"><span data-stu-id="e8018-122">Specifies the load balancing method to use to distribute the connection.</span></span>
<span data-ttu-id="e8018-123">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="e8018-123">Valid values are:</span></span> 

- <span data-ttu-id="e8018-124">Pracy</span><span class="sxs-lookup"><span data-stu-id="e8018-124">Performance</span></span>
- <span data-ttu-id="e8018-125">Jęcie</span><span class="sxs-lookup"><span data-stu-id="e8018-125">Failover</span></span>
- <span data-ttu-id="e8018-126">RoundRobin</span><span class="sxs-lookup"><span data-stu-id="e8018-126">RoundRobin</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8018-127">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="e8018-127">-MonitorPort</span></span>
<span data-ttu-id="e8018-128">Określa port służący do monitorowania kondycji punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="e8018-128">Specifies the port used to monitor endpoint health.</span></span>
<span data-ttu-id="e8018-129">Prawidłowe wartości to wartości całkowite większe niż 0 i mniejsze niż lub równe 65 535.</span><span class="sxs-lookup"><span data-stu-id="e8018-129">Valid values are integer values greater than 0 and less than or equal to 65,535.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8018-130">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="e8018-130">-MonitorProtocol</span></span>
<span data-ttu-id="e8018-131">Określa protokół, który ma być używany do monitorowania kondycji punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="e8018-131">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="e8018-132">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="e8018-132">Valid values are:</span></span> 

- <span data-ttu-id="e8018-133">URL</span><span class="sxs-lookup"><span data-stu-id="e8018-133">Http</span></span>

- <span data-ttu-id="e8018-134">Https</span><span class="sxs-lookup"><span data-stu-id="e8018-134">Https</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8018-135">-MonitorRelativePath</span><span class="sxs-lookup"><span data-stu-id="e8018-135">-MonitorRelativePath</span></span>
<span data-ttu-id="e8018-136">Określa ścieżkę względem nazwy domeny punktu końcowego do sondowania stanu kondycji.</span><span class="sxs-lookup"><span data-stu-id="e8018-136">Specifies the path relative to the endpoint domain name to probe for health state.</span></span>
<span data-ttu-id="e8018-137">Ścieżka musi być zgodna z następującymi ograniczeniami:</span><span class="sxs-lookup"><span data-stu-id="e8018-137">The path must meet the following restrictions:</span></span> 

- <span data-ttu-id="e8018-138">Ścieżka musi zawierać od 1 do 1000 znaków.</span><span class="sxs-lookup"><span data-stu-id="e8018-138">The path must be from 1 through 1000 characters.</span></span>

- <span data-ttu-id="e8018-139">Musi zaczynać się ukośnikiem/.</span><span class="sxs-lookup"><span data-stu-id="e8018-139">It must start with a forward slash, /.</span></span>

- <span data-ttu-id="e8018-140">Nie może zawierać żadnych elementów XML \<\> .</span><span class="sxs-lookup"><span data-stu-id="e8018-140">It must contain no XML elements, \<\>.</span></span>

- <span data-ttu-id="e8018-141">Nie może zawierać podwójnych ukośników,//.</span><span class="sxs-lookup"><span data-stu-id="e8018-141">It must contain no double slashes, //.</span></span>

- <span data-ttu-id="e8018-142">Nie może zawierać nieprawidłowych znaków escape HTML.</span><span class="sxs-lookup"><span data-stu-id="e8018-142">It must contain no invalid HTML escape characters.</span></span>
<span data-ttu-id="e8018-143">Na przykład% XY.</span><span class="sxs-lookup"><span data-stu-id="e8018-143">For example, %XY.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8018-144">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e8018-144">-Name</span></span>
<span data-ttu-id="e8018-145">Określa nazwę profilu usługi Traffic Manager, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="e8018-145">Specifies the name of the Traffic Manager profile to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8018-146">-Profile</span><span class="sxs-lookup"><span data-stu-id="e8018-146">-Profile</span></span>
<span data-ttu-id="e8018-147">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8018-147">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="e8018-148">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="e8018-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8018-149">-TTL</span><span class="sxs-lookup"><span data-stu-id="e8018-149">-Ttl</span></span>
<span data-ttu-id="e8018-150">Określa czas wygaśnięcia (TTL) DNS, który informuje lokalnych nazw DNS, jak długo są buforowane wpisy DNS.</span><span class="sxs-lookup"><span data-stu-id="e8018-150">Specifies the DNS Time-to-Live (TTL) that informs the Local DNS resolvers how long to cache DNS entries.</span></span>
<span data-ttu-id="e8018-151">Prawidłowe wartości to liczby całkowite z zakresu od 30 do 999 999.</span><span class="sxs-lookup"><span data-stu-id="e8018-151">Valid values are integers from 30 through 999,999.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8018-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8018-152">CommonParameters</span></span>
<span data-ttu-id="e8018-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8018-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8018-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8018-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8018-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8018-155">INPUTS</span></span>

## <span data-ttu-id="e8018-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e8018-156">OUTPUTS</span></span>

### <span data-ttu-id="e8018-157">Microsoft. platformy windowsazure. Commands. Utilities.. modele. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="e8018-157">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="e8018-158">To polecenie cmdlet generuje obiekt profilu programu Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="e8018-158">This cmdlet generates a Traffic Manager profile object.</span></span>

## <span data-ttu-id="e8018-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e8018-159">NOTES</span></span>

## <span data-ttu-id="e8018-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8018-160">RELATED LINKS</span></span>

[<span data-ttu-id="e8018-161">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e8018-161">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="e8018-162">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e8018-162">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="e8018-163">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e8018-163">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="e8018-164">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e8018-164">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="e8018-165">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e8018-165">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


