---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: FAEA7859-7E58-4343-AD57-7EFC0D87432E
online version: ''
schema: 2.0.0
ms.openlocfilehash: d2886faacd3e9f7d02a008a056dc2145844f8b30
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054400"
---
# <span data-ttu-id="021ea-101">Set-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="021ea-101">Set-AzureTrafficManagerEndpoint</span></span>

## <span data-ttu-id="021ea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="021ea-102">SYNOPSIS</span></span>
<span data-ttu-id="021ea-103">Aktualizuje właściwości punktu końcowego w profilu usługi Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="021ea-103">Updates the properties of an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="021ea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="021ea-104">SYNTAX</span></span>

```
Set-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] [-Type <String>] [-Status <String>]
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="021ea-105">Opis</span><span class="sxs-lookup"><span data-stu-id="021ea-105">DESCRIPTION</span></span>
<span data-ttu-id="021ea-106">Polecenie cmdlet **Set-AzureTrafficManagerEndpoint** aktualizuje właściwości punktu końcowego w profilu programu Microsoft Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="021ea-106">The **Set-AzureTrafficManagerEndpoint** cmdlet updates the properties of an endpoint in a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="021ea-107">Jeśli punkt końcowy nie istnieje w bieżącym profilu, to polecenie cmdlet utworzy je.</span><span class="sxs-lookup"><span data-stu-id="021ea-107">If the endpoint does not exist in the current profile, this cmdlet creates it.</span></span>
<span data-ttu-id="021ea-108">Po dodaniu punktu końcowego przekazanie wyniku do polecenia cmdlet **Set-AzureTrafficManagerProfile** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="021ea-108">After you add an endpoint, pass the result to the **Set-AzureTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="021ea-109">To polecenie cmdlet łączy się z usługą Azure, aby zapisać zmiany.</span><span class="sxs-lookup"><span data-stu-id="021ea-109">That cmdlet connects to Azure to save your changes.</span></span>

## <span data-ttu-id="021ea-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="021ea-110">EXAMPLES</span></span>

### <span data-ttu-id="021ea-111">Przykład 1: aktualizowanie punktu końcowego dla profilu</span><span class="sxs-lookup"><span data-stu-id="021ea-111">Example 1: Update an endpoint for a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Set-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "ContosoApp02.cloudapp.net" -Status "Enabled" -Type "CloudService" -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="021ea-112">W pierwszym poleceniu jest używany polecenie cmdlet **Get-AzureTrafficManagerProfile** w celu uzyskania profilu o nazwie ContosoProfile, a następnie zapisanie go w zmiennej $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="021ea-112">The first command uses the **Get-AzureTrafficManagerProfile** cmdlet to get the profile named ContosoProfile, and then stores it in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="021ea-113">Drugie polecenie aktualizuje punkt końcowy w profilu usługi Traffic Manager przechowywanych w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="021ea-113">The second command updates the endpoint in the Traffic Manager profile that is stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="021ea-114">Punkt końcowy ma nazwę domeny ContosoApp02.cloudapp.net.</span><span class="sxs-lookup"><span data-stu-id="021ea-114">The endpoint has the domain name ContosoApp02.cloudapp.net.</span></span>
<span data-ttu-id="021ea-115">Polecenie określa również stan, typ, wagę i lokalizację punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="021ea-115">The command also specifies the status, type, weight, and location of the endpoint.</span></span>
<span data-ttu-id="021ea-116">Polecenie przekazuje zmodyfikowany profil do polecenia cmdlet **Set-AzureTrafficManagerProfile** , aby połączyć się z usługą Azure w celu zapisania zmian.</span><span class="sxs-lookup"><span data-stu-id="021ea-116">The command passes the modified profile to the **Set-AzureTrafficManagerProfile** cmdlet to connect to Azure to save your changes.</span></span>

## <span data-ttu-id="021ea-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="021ea-117">PARAMETERS</span></span>

### <span data-ttu-id="021ea-118">-NazwaDomeny</span><span class="sxs-lookup"><span data-stu-id="021ea-118">-DomainName</span></span>
<span data-ttu-id="021ea-119">Określa nazwę domeny punktu końcowego, który należy zmodyfikować.</span><span class="sxs-lookup"><span data-stu-id="021ea-119">Specifies the domain name of the endpoint to modify.</span></span>

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

### <span data-ttu-id="021ea-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="021ea-120">-Location</span></span>
<span data-ttu-id="021ea-121">Określa lokalizację punktu końcowego, który jest dodawany przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="021ea-121">Specifies the location of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="021ea-122">To musi być lokalizacja na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="021ea-122">This must be an Azure location.</span></span>

<span data-ttu-id="021ea-123">Ten parametr musi zawierać wartość dla punktów końcowych typu "any" lub typu "Trafficmanager" w profilu, którego Metoda równoważenia obciążenia jest ustawiona na wartość "wydajność".</span><span class="sxs-lookup"><span data-stu-id="021ea-123">This parameter must contain a value for endpoints of the type "Any" or of type "TrafficManager" in a profile that has the load balancing method set to "Performance".</span></span>
<span data-ttu-id="021ea-124">Możliwe wartości to nazwy regionów platformy Azure, które wymieniono na liście  https://azure.microsoft.com/regions/https://azure.microsoft.com/regions/ .</span><span class="sxs-lookup"><span data-stu-id="021ea-124">The possible values are the Azure region names, as listed at  https://azure.microsoft.com/regions/https://azure.microsoft.com/regions/.</span></span>

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

### <span data-ttu-id="021ea-125">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="021ea-125">-MinChildEndpoints</span></span>
<span data-ttu-id="021ea-126">Określa minimalną liczbę punktów końcowych, które profil zagnieżdżony musi mieć w trybie online, aby ten punkt końcowy był traktowany jako dostępny.</span><span class="sxs-lookup"><span data-stu-id="021ea-126">Specifies the minimum number of endpoints the nested profile must have online for this endpoint to be considered online.</span></span>

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

### <span data-ttu-id="021ea-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="021ea-127">-Profile</span></span>
<span data-ttu-id="021ea-128">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="021ea-128">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="021ea-129">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="021ea-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="021ea-130">-Status</span><span class="sxs-lookup"><span data-stu-id="021ea-130">-Status</span></span>
<span data-ttu-id="021ea-131">Określa stan punktu końcowego monitorowania.</span><span class="sxs-lookup"><span data-stu-id="021ea-131">Specifies the status of the monitoring endpoint.</span></span>
<span data-ttu-id="021ea-132">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="021ea-132">Valid values are:</span></span> 

- <span data-ttu-id="021ea-133">Wyłączona</span><span class="sxs-lookup"><span data-stu-id="021ea-133">Enabled</span></span>
- <span data-ttu-id="021ea-134">Łącza</span><span class="sxs-lookup"><span data-stu-id="021ea-134">Disabled</span></span>

<span data-ttu-id="021ea-135">Jeśli określisz wartość włączone, Usługa Traffic Manager monitoruje punkt końcowy, a metoda równoważenia obciążenia traktuje ją podczas zarządzania ruchem.</span><span class="sxs-lookup"><span data-stu-id="021ea-135">If you specify a value of Enabled, Traffic Manager monitors the endpoint and the load-balancing method considers it when managing traffic.</span></span>

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

### <span data-ttu-id="021ea-136">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="021ea-136">-TrafficManagerProfile</span></span>
<span data-ttu-id="021ea-137">Określa obiekt profilu usługi Traffic Manager, dla którego ma zostać zmodyfikowany punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="021ea-137">Specifies the Traffic Manager profile object for which to modify the endpoint.</span></span>

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

### <span data-ttu-id="021ea-138">-Type</span><span class="sxs-lookup"><span data-stu-id="021ea-138">-Type</span></span>
<span data-ttu-id="021ea-139">Określa typ punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="021ea-139">Specifies the type of endpoint.</span></span>
<span data-ttu-id="021ea-140">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="021ea-140">Valid values are:</span></span> 

- <span data-ttu-id="021ea-141">CloudService</span><span class="sxs-lookup"><span data-stu-id="021ea-141">CloudService</span></span>
- <span data-ttu-id="021ea-142">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="021ea-142">AzureWebsite</span></span>
- <span data-ttu-id="021ea-143">Nr ruchu</span><span class="sxs-lookup"><span data-stu-id="021ea-143">TrafficManager</span></span>

- <span data-ttu-id="021ea-144">Jakieś</span><span class="sxs-lookup"><span data-stu-id="021ea-144">Any</span></span> 

<span data-ttu-id="021ea-145">Jeśli istnieje więcej niż jeden punkt końcowy AzureWebsite, punkty końcowe muszą znajdować się w różnych centrach danych.</span><span class="sxs-lookup"><span data-stu-id="021ea-145">If there is more than one AzureWebsite endpoint, the endpoints must be in different datacenters.</span></span>

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

### <span data-ttu-id="021ea-146">-Waga</span><span class="sxs-lookup"><span data-stu-id="021ea-146">-Weight</span></span>
<span data-ttu-id="021ea-147">Określa wagę punktu końcowego, który jest dodawany przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="021ea-147">Specifies the weight of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="021ea-148">Prawidłowy zakres wartości dla tego parametru to \[ 1, 1000 \] .</span><span class="sxs-lookup"><span data-stu-id="021ea-148">The valid value range for this parameter is \[1,1000\].</span></span>

<span data-ttu-id="021ea-149">Ten parametr jest wykorzystywany tylko w przypadku zasad równoważenia obciążenia RoundRobin.</span><span class="sxs-lookup"><span data-stu-id="021ea-149">This parameter is only used for RoundRobin load balancing policies.</span></span>

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

### <span data-ttu-id="021ea-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="021ea-150">CommonParameters</span></span>
<span data-ttu-id="021ea-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="021ea-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="021ea-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="021ea-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="021ea-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="021ea-153">INPUTS</span></span>

## <span data-ttu-id="021ea-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="021ea-154">OUTPUTS</span></span>

### <span data-ttu-id="021ea-155">Microsoft. platformy windowsazure. Commands. Utilities.. modele. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="021ea-155">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="021ea-156">To polecenie cmdlet generuje obiekt profilu usługi Traffic Manager, który zawiera informacje na temat zaktualizowanego profilu.</span><span class="sxs-lookup"><span data-stu-id="021ea-156">This cmdlet generates a Traffic Manager profile object, which contains information about the updated profile.</span></span>

## <span data-ttu-id="021ea-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="021ea-157">NOTES</span></span>

## <span data-ttu-id="021ea-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="021ea-158">RELATED LINKS</span></span>

[<span data-ttu-id="021ea-159">Dodaj-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="021ea-159">Add-AzureTrafficManagerEndpoint</span></span>](./Add-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="021ea-160">Remove-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="021ea-160">Remove-AzureTrafficManagerEndpoint</span></span>](./Remove-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="021ea-161">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="021ea-161">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="021ea-162">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="021ea-162">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


