---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 700AC44E-4FD5-4516-80F3-B8C9E4DF6ABC
online version: ''
schema: 2.0.0
ms.openlocfilehash: d37397b4e0ce9f1d9878860eb5e7a431e58a20a9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054760"
---
# <span data-ttu-id="101d9-101">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="101d9-101">Set-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="101d9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="101d9-102">SYNOPSIS</span></span>
<span data-ttu-id="101d9-103">Aktualizuje właściwości profilu usługi Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="101d9-103">Updates the properties of a Traffic Manager profile.</span></span>

## <span data-ttu-id="101d9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="101d9-104">SYNTAX</span></span>

```
Set-AzureTrafficManagerProfile [-Name <String>] [-LoadBalancingMethod <String>] [-MonitorPort <Int32>]
 [-MonitorProtocol <String>] [-MonitorRelativePath <String>] [-Ttl <Int32>]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="101d9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="101d9-105">DESCRIPTION</span></span>
<span data-ttu-id="101d9-106">Polecenie cmdlet **Set-AzureTrafficManagerProfile** aktualizuje właściwości profilu Microsoft Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="101d9-106">The **Set-AzureTrafficManagerProfile** cmdlet updates the properties of a Microsoft Azure Traffic Manager profile.</span></span>

<span data-ttu-id="101d9-107">W przypadku profilów, dla których ustawiono wartość *LoadBalancingMethod* na "tryb failover", możesz określić kolejność przejęcia awaryjnego punktów końcowych dodanych do profilu za pomocą polecenia cmdlet Add-AzureTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="101d9-107">For profiles for which you have set the *LoadBalancingMethod* value to "Failover", you can determine the failover order of the endpoints you have added to your profile with the Add-AzureTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="101d9-108">Aby uzyskać więcej informacji, zobacz przykład 3 poniżej.</span><span class="sxs-lookup"><span data-stu-id="101d9-108">For more information, see Example 3 below.</span></span>

## <span data-ttu-id="101d9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="101d9-109">EXAMPLES</span></span>

### <span data-ttu-id="101d9-110">Przykład 1: Ustawianie wartości TTL dla profilu usługi Traffic Manager</span><span class="sxs-lookup"><span data-stu-id="101d9-110">Example 1: Set the TTL for a Traffic Manager profile</span></span>
```
PS C:\>Set-AzureTrafficManagerProfile -TrafficManagerProfile $MyTrafficManagerProfile -Ttl 60
```

<span data-ttu-id="101d9-111">To polecenie ustawia wartość TTL równą 60 sekund dla obiektu profilu usługi Traffic Manager MyTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="101d9-111">This command sets the TTL to 60 seconds for the Traffic Manager profile object MyTrafficManagerProfile.</span></span>

### <span data-ttu-id="101d9-112">Przykład 2: Ustawianie kilku wartości dla profilu</span><span class="sxs-lookup"><span data-stu-id="101d9-112">Example 2: Set several values for a profile</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Set-AzureTrafficManagerProfile -LoadBalancingMethod "RoundRobin" -Ttl 30 -MonitorProtocol "Http" -MonitorPort 80 -MonitorRelativePath "/"
```

<span data-ttu-id="101d9-113">To polecenie pobiera profil usługi Traffic Manager o nazwie Moja profil przy użyciu polecenia cmdlet **Get-AzureTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="101d9-113">This command gets a Traffic Manager profile named MyProfile by using the **Get-AzureTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="101d9-114">W profilu jest używana metoda równoważenia obciążenia RoundRobin, czyli czas wygaśnięcia: 30 sekund, protokół monitorowania HTTP, port monitora i ścieżka względna profilu usługi Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="101d9-114">The profile uses the RoundRobin load balancing method, a TTL of 30 seconds,  the monitor protocol HTTP, the monitor port, and the relative path for a Traffic Manager profile.</span></span>

### <span data-ttu-id="101d9-115">Przykład 3: Zmienianie kolejności punktów końcowych na pożądaną kolejność w trybie failover</span><span class="sxs-lookup"><span data-stu-id="101d9-115">Example 3: Reorder endpoints to desired failover order</span></span>
```
PS C:\>$Profile = Get-AzureTrafficManagerProfile -Name "MyProfile"
PS C:\> $Profile.Endpoints[0],$Profile.Endpoints[1] = $Profile.Endpoints[1],$Profile.Endpoints[0]
PS C:\> $Profile = Set-AzureTrafficManagerProfile
```

<span data-ttu-id="101d9-116">Ten przykład zmienia kolejność punktów końcowych dodanych do polecenia mój profil do wybranego zlecenia trybu failover.</span><span class="sxs-lookup"><span data-stu-id="101d9-116">This example reorders the endpoints added to MyProfile to the desired failover order.</span></span>

<span data-ttu-id="101d9-117">Pierwsze polecenie pobiera obiekt profilu usługi Traffic Manager o nazwie Moja profil i zapisuje obiekt w zmiennej $Profile.</span><span class="sxs-lookup"><span data-stu-id="101d9-117">The first command gets the Traffic Manager profile object named MyProfile and stores the object in the $Profile variable.</span></span>

<span data-ttu-id="101d9-118">Drugie polecenie ponownie porządkuje punkty końcowe z tablicy punktów końcowych do kolejności, w której ma się odbywać przejście.</span><span class="sxs-lookup"><span data-stu-id="101d9-118">The second command re-orders the endpoints from  the endpoints array to the order in which failover should occur.</span></span>

<span data-ttu-id="101d9-119">Ostatnie polecenie aktualizuje profil usługi Traffic Manager przechowywany w $Profile z nową kolejnością punktów końcowych.</span><span class="sxs-lookup"><span data-stu-id="101d9-119">The last command updates the Traffic Manager profile stored in $Profile with the new endpoint order.</span></span>

## <span data-ttu-id="101d9-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="101d9-120">PARAMETERS</span></span>

### <span data-ttu-id="101d9-121">-LoadBalancingMethod</span><span class="sxs-lookup"><span data-stu-id="101d9-121">-LoadBalancingMethod</span></span>
<span data-ttu-id="101d9-122">Określa metodę równoważenia obciążenia używaną do rozpowszechniania połączenia.</span><span class="sxs-lookup"><span data-stu-id="101d9-122">Specifies the load balancing method to use to distribute the connection.</span></span>
<span data-ttu-id="101d9-123">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="101d9-123">Valid values are:</span></span> 

- <span data-ttu-id="101d9-124">Pracy</span><span class="sxs-lookup"><span data-stu-id="101d9-124">Performance</span></span>
- <span data-ttu-id="101d9-125">Jęcie</span><span class="sxs-lookup"><span data-stu-id="101d9-125">Failover</span></span>
- <span data-ttu-id="101d9-126">RoundRobin</span><span class="sxs-lookup"><span data-stu-id="101d9-126">RoundRobin</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="101d9-127">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="101d9-127">-MonitorPort</span></span>
<span data-ttu-id="101d9-128">Określa port służący do monitorowania kondycji punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="101d9-128">Specifies the port used to monitor endpoint health.</span></span>
<span data-ttu-id="101d9-129">Prawidłowe wartości to wartości całkowite większe niż 0 i mniejsze niż lub równe 65 535.</span><span class="sxs-lookup"><span data-stu-id="101d9-129">Valid values are integer values greater than 0 and less than or equal to 65,535.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="101d9-130">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="101d9-130">-MonitorProtocol</span></span>
<span data-ttu-id="101d9-131">Określa protokół, który ma być używany do monitorowania kondycji punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="101d9-131">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="101d9-132">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="101d9-132">Valid values are:</span></span> 

- <span data-ttu-id="101d9-133">URL</span><span class="sxs-lookup"><span data-stu-id="101d9-133">Http</span></span>
- <span data-ttu-id="101d9-134">Https</span><span class="sxs-lookup"><span data-stu-id="101d9-134">Https</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="101d9-135">-MonitorRelativePath</span><span class="sxs-lookup"><span data-stu-id="101d9-135">-MonitorRelativePath</span></span>
<span data-ttu-id="101d9-136">Określa ścieżkę względem nazwy domeny punktu końcowego do sondowania stanu kondycji.</span><span class="sxs-lookup"><span data-stu-id="101d9-136">Specifies the path relative to the endpoint domain name to probe for health state.</span></span>
<span data-ttu-id="101d9-137">Ścieżka musi być zgodna z następującymi ograniczeniami:</span><span class="sxs-lookup"><span data-stu-id="101d9-137">The path must meet the following restrictions:</span></span> 

- <span data-ttu-id="101d9-138">Ścieżka musi zawierać od 1 do 1000 znaków.</span><span class="sxs-lookup"><span data-stu-id="101d9-138">The path must be from 1 through 1000 characters.</span></span>
- <span data-ttu-id="101d9-139">Musi zaczynać się ukośnikiem/.</span><span class="sxs-lookup"><span data-stu-id="101d9-139">It must start with a forward slash, /.</span></span>
- <span data-ttu-id="101d9-140">Nie może zawierać żadnych elementów XML \<\> .</span><span class="sxs-lookup"><span data-stu-id="101d9-140">It must contain no XML elements, \<\>.</span></span>
- <span data-ttu-id="101d9-141">Nie może zawierać podwójnych ukośników,//.</span><span class="sxs-lookup"><span data-stu-id="101d9-141">It must contain no double slashes, //.</span></span>
- <span data-ttu-id="101d9-142">Nie może zawierać nieprawidłowych znaków escape HTML.</span><span class="sxs-lookup"><span data-stu-id="101d9-142">It must contain no invalid HTML escape characters.</span></span>
<span data-ttu-id="101d9-143">Na przykład% XY.</span><span class="sxs-lookup"><span data-stu-id="101d9-143">For example, %XY.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="101d9-144">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="101d9-144">-Name</span></span>
<span data-ttu-id="101d9-145">Określa nazwę profilu usługi Traffic Manager do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="101d9-145">Specifies the name of the Traffic Manager profile to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="101d9-146">-Profile</span><span class="sxs-lookup"><span data-stu-id="101d9-146">-Profile</span></span>
<span data-ttu-id="101d9-147">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="101d9-147">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="101d9-148">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="101d9-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="101d9-149">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="101d9-149">-TrafficManagerProfile</span></span>
<span data-ttu-id="101d9-150">Określa obiekt profilu usługi Traffic Manager używany do ustawiania profilu.</span><span class="sxs-lookup"><span data-stu-id="101d9-150">Specifies the Traffic Manager profile object you use to set the profile.</span></span>

```yaml
Type: IProfileWithDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="101d9-151">-TTL</span><span class="sxs-lookup"><span data-stu-id="101d9-151">-Ttl</span></span>
<span data-ttu-id="101d9-152">Określa czas wygaśnięcia (TTL) DNS, który informuje lokalnych nazw DNS, jak długo są buforowane wpisy DNS.</span><span class="sxs-lookup"><span data-stu-id="101d9-152">Specifies the DNS Time-to-Live (TTL) that informs the Local DNS resolvers how long to cache DNS entries.</span></span>
<span data-ttu-id="101d9-153">Prawidłowe wartości to liczby całkowite z zakresu od 30 do 999 999.</span><span class="sxs-lookup"><span data-stu-id="101d9-153">Valid values are an integer from 30 through 999,999.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="101d9-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="101d9-154">CommonParameters</span></span>
<span data-ttu-id="101d9-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="101d9-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="101d9-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="101d9-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="101d9-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="101d9-157">INPUTS</span></span>

## <span data-ttu-id="101d9-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="101d9-158">OUTPUTS</span></span>

### <span data-ttu-id="101d9-159">Microsoft. platformy windowsazure. Commands. Utilities.. modele. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="101d9-159">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="101d9-160">To polecenie cmdlet generuje obiekt profilu programu Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="101d9-160">This cmdlet generates a Traffic Manager profile object.</span></span>

## <span data-ttu-id="101d9-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="101d9-161">NOTES</span></span>

## <span data-ttu-id="101d9-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="101d9-162">RELATED LINKS</span></span>

[<span data-ttu-id="101d9-163">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="101d9-163">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="101d9-164">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="101d9-164">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="101d9-165">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="101d9-165">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="101d9-166">Nowe — AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="101d9-166">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="101d9-167">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="101d9-167">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)


