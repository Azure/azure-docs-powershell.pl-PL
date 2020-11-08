---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: CF1FC482-812D-4BAD-BA3A-D88E614A5165
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79f212e83ece1def42c6d8de343a42e087f5181a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055342"
---
# <span data-ttu-id="57bad-101">Add-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="57bad-101">Add-AzureTrafficManagerEndpoint</span></span>

## <span data-ttu-id="57bad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="57bad-102">SYNOPSIS</span></span>
<span data-ttu-id="57bad-103">Dodaje punkt końcowy do profilu usługi Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="57bad-103">Adds an endpoint to a Traffic Manager profile.</span></span>

## <span data-ttu-id="57bad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="57bad-104">SYNTAX</span></span>

```
Add-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] -Type <String> -Status <String>
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="57bad-105">Opis</span><span class="sxs-lookup"><span data-stu-id="57bad-105">DESCRIPTION</span></span>
<span data-ttu-id="57bad-106">Polecenie cmdlet **Add-AzureTrafficManagerEndpoint** umożliwia dodanie punktu końcowego do profilu usługi Microsoft Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="57bad-106">The **Add-AzureTrafficManagerEndpoint** cmdlet adds an endpoint to a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="57bad-107">Po dodaniu punktu końcowego przekazanie wyniku do polecenia cmdlet **Set-AzureTrafficManagerProfile** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="57bad-107">After you add an endpoint, pass the result to the **Set-AzureTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="57bad-108">To polecenie cmdlet łączy się z usługą Azure, aby zapisać zmiany.</span><span class="sxs-lookup"><span data-stu-id="57bad-108">That cmdlet connects to Azure to save your changes.</span></span>

## <span data-ttu-id="57bad-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="57bad-109">EXAMPLES</span></span>

### <span data-ttu-id="57bad-110">Przykład 1. Dodawanie punktu końcowego do profilu</span><span class="sxs-lookup"><span data-stu-id="57bad-110">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Add-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" -Status "Enabled" -Type "CloudService" | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="57bad-111">W pierwszym poleceniu jest używany polecenie cmdlet **Get-AzureTrafficManagerProfile** w celu uzyskania profilu o nazwie ContosoProfile, a następnie zapisanie go w zmiennej $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="57bad-111">The first command uses the **Get-AzureTrafficManagerProfile** cmdlet to get the profile named ContosoProfile, and then stores it in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="57bad-112">Drugie polecenie dodaje punkt końcowy do profilu usługi Traffic Manager przechowywanego w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="57bad-112">The second command adds an endpoint to Traffic Manager profile that is stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="57bad-113">Punkt końcowy ma nazwę domeny Contoso02App.couldapp.net.</span><span class="sxs-lookup"><span data-stu-id="57bad-113">The endpoint has the domain name Contoso02App.couldapp.net.</span></span>
<span data-ttu-id="57bad-114">To polecenie określa również, czy jest włączone, oraz typ.</span><span class="sxs-lookup"><span data-stu-id="57bad-114">The command also specifies whether it is enabled and its type.</span></span>
<span data-ttu-id="57bad-115">Polecenie przekazuje obiekt profilu do polecenia cmdlet **Set-AzureTrafficManagerProfile** , aby połączyć się z usługą Azure w celu zapisania zmian.</span><span class="sxs-lookup"><span data-stu-id="57bad-115">The command passes the profile object to the **Set-AzureTrafficManagerProfile** cmdlet to connect to Azure to save your changes.</span></span>

### <span data-ttu-id="57bad-116">Przykład 2: Dodawanie punktu końcowego z określoną lokalizacją i wagą</span><span class="sxs-lookup"><span data-stu-id="57bad-116">Example 2: Add an endpoint that has a specified location and weight</span></span>
```
PS C:\>Add-AzureTrafficManagerEndpoint -TrafficManagerProfile ContosoTrafficManagerProfile -DomainName " Contoso02App.cloudapp.net" -Status Enabled -Type CloudService -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="57bad-117">To polecenie umożliwia dodanie punktu końcowego do profilu usługi Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="57bad-117">This command adds an endpoint to a Traffic Manager profile.</span></span>
<span data-ttu-id="57bad-118">Punkt końcowy ma nazwę domeny Contoso02App.couldapp.net.</span><span class="sxs-lookup"><span data-stu-id="57bad-118">The endpoint has the domain name Contoso02App.couldapp.net.</span></span>
<span data-ttu-id="57bad-119">To polecenie określa również, czy jest włączone, oraz typ.</span><span class="sxs-lookup"><span data-stu-id="57bad-119">The command also specifies whether it is enabled and its type.</span></span>
<span data-ttu-id="57bad-120">Polecenie określa również wagę i lokalizację punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="57bad-120">The command also specifies the weight and location for the endpoint.</span></span>
<span data-ttu-id="57bad-121">Polecenie przekazuje obiekt profilu w celu **Ustawienia — AzureTrafficManagerProfile** , aby połączyć się z usługą Azure w celu zapisania zmian.</span><span class="sxs-lookup"><span data-stu-id="57bad-121">The command passes the profile object to **Set-AzureTrafficManagerProfile** to connect to Azure to save your changes.</span></span>

## <span data-ttu-id="57bad-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="57bad-122">PARAMETERS</span></span>

### <span data-ttu-id="57bad-123">-NazwaDomeny</span><span class="sxs-lookup"><span data-stu-id="57bad-123">-DomainName</span></span>
<span data-ttu-id="57bad-124">Określa nazwę domeny punktu końcowego, który ma zostać dodany.</span><span class="sxs-lookup"><span data-stu-id="57bad-124">Specifies the domain name of the endpoint to add.</span></span>

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

### <span data-ttu-id="57bad-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="57bad-125">-Location</span></span>
<span data-ttu-id="57bad-126">Określa lokalizację punktu końcowego, który jest dodawany przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57bad-126">Specifies the location of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="57bad-127">To musi być lokalizacja na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="57bad-127">This must be an Azure location.</span></span>

<span data-ttu-id="57bad-128">Ten parametr musi zawierać wartość dla punktów końcowych typu "any" lub typu "Trafficmanager" w profilu, którego Metoda równoważenia obciążenia jest ustawiona na wartość "wydajność".</span><span class="sxs-lookup"><span data-stu-id="57bad-128">This parameter must contain a value for endpoints of the type "Any" or of type "TrafficManager" in a profile that has the load balancing method set to "Performance".</span></span>
<span data-ttu-id="57bad-129">Możliwe wartości to nazwy regionów platformy Azure, które wymieniono na liście https://azure.microsoft.com/regions/ .</span><span class="sxs-lookup"><span data-stu-id="57bad-129">The possible values are the Azure region names, as listed at https://azure.microsoft.com/regions/.</span></span>

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

### <span data-ttu-id="57bad-130">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="57bad-130">-MinChildEndpoints</span></span>
<span data-ttu-id="57bad-131">Określa minimalną liczbę punktów końcowych, które profil zagnieżdżony musi mieć w trybie online, aby ten punkt końcowy był traktowany jako dostępny.</span><span class="sxs-lookup"><span data-stu-id="57bad-131">Specifies the minimum number of endpoints the nested profile must have online for this endpoint to be considered online.</span></span>

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

### <span data-ttu-id="57bad-132">-Profile</span><span class="sxs-lookup"><span data-stu-id="57bad-132">-Profile</span></span>
<span data-ttu-id="57bad-133">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57bad-133">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="57bad-134">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="57bad-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="57bad-135">-Status</span><span class="sxs-lookup"><span data-stu-id="57bad-135">-Status</span></span>
<span data-ttu-id="57bad-136">Określa stan punktu końcowego monitorowania.</span><span class="sxs-lookup"><span data-stu-id="57bad-136">Specifies the status of the monitoring endpoint.</span></span>
<span data-ttu-id="57bad-137">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="57bad-137">Valid values are:</span></span> 

- <span data-ttu-id="57bad-138">Wyłączona</span><span class="sxs-lookup"><span data-stu-id="57bad-138">Enabled</span></span>
- <span data-ttu-id="57bad-139">Łącza</span><span class="sxs-lookup"><span data-stu-id="57bad-139">Disabled</span></span>

<span data-ttu-id="57bad-140">Jeśli określisz wartość włączone, Usługa Traffic Manager monitoruje punkt końcowy, a metoda równoważenia obciążenia traktuje ją podczas zarządzania ruchem.</span><span class="sxs-lookup"><span data-stu-id="57bad-140">If you specify a value of Enabled, Traffic Manager monitors the endpoint and the load-balancing method considers it when managing traffic.</span></span>

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

### <span data-ttu-id="57bad-141">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="57bad-141">-TrafficManagerProfile</span></span>
<span data-ttu-id="57bad-142">Określa obiekt profilu usługi Traffic Manager, do którego ma zostać dodany punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="57bad-142">Specifies the Traffic Manager profile object to which to add the endpoint.</span></span>

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

### <span data-ttu-id="57bad-143">-Type</span><span class="sxs-lookup"><span data-stu-id="57bad-143">-Type</span></span>
<span data-ttu-id="57bad-144">Określa typ punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="57bad-144">Specifies the type of endpoint.</span></span>
<span data-ttu-id="57bad-145">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="57bad-145">Valid values are:</span></span> 

- <span data-ttu-id="57bad-146">CloudService</span><span class="sxs-lookup"><span data-stu-id="57bad-146">CloudService</span></span>
- <span data-ttu-id="57bad-147">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="57bad-147">AzureWebsite</span></span>
- <span data-ttu-id="57bad-148">Nr ruchu</span><span class="sxs-lookup"><span data-stu-id="57bad-148">TrafficManager</span></span>

- <span data-ttu-id="57bad-149">Jakieś</span><span class="sxs-lookup"><span data-stu-id="57bad-149">Any</span></span> 

<span data-ttu-id="57bad-150">Jeśli istnieje więcej niż jeden punkt końcowy AzureWebsite, punkty końcowe muszą znajdować się w różnych centrach danych.</span><span class="sxs-lookup"><span data-stu-id="57bad-150">If there is more than one AzureWebsite endpoint, the endpoints must be in different datacenters.</span></span>

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

### <span data-ttu-id="57bad-151">-Waga</span><span class="sxs-lookup"><span data-stu-id="57bad-151">-Weight</span></span>
<span data-ttu-id="57bad-152">Określa wagę punktu końcowego, który jest dodawany przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57bad-152">Specifies the weight of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="57bad-153">Prawidłowy zakres wartości dla tego parametru to \[ 1, 1000 \] .</span><span class="sxs-lookup"><span data-stu-id="57bad-153">The valid value range for this parameter is \[1,1000\].</span></span>

<span data-ttu-id="57bad-154">Ten parametr jest wykorzystywany tylko w przypadku zasad równoważenia obciążenia RoundRobin.</span><span class="sxs-lookup"><span data-stu-id="57bad-154">This parameter is only used for RoundRobin load balancing policies.</span></span>

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

### <span data-ttu-id="57bad-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57bad-155">CommonParameters</span></span>
<span data-ttu-id="57bad-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57bad-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57bad-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57bad-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57bad-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57bad-158">INPUTS</span></span>

## <span data-ttu-id="57bad-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="57bad-159">OUTPUTS</span></span>

### <span data-ttu-id="57bad-160">Microsoft. platformy windowsazure. Commands. Utilities.. modele. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="57bad-160">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="57bad-161">To polecenie cmdlet generuje obiekt profilu usługi Traffic Manager, który zawiera informacje na temat zaktualizowanego profilu.</span><span class="sxs-lookup"><span data-stu-id="57bad-161">This cmdlet generates a Traffic Manager profile object, which contains information about the updated profile.</span></span>

## <span data-ttu-id="57bad-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="57bad-162">NOTES</span></span>

## <span data-ttu-id="57bad-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57bad-163">RELATED LINKS</span></span>

[<span data-ttu-id="57bad-164">Remove-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="57bad-164">Remove-AzureTrafficManagerEndpoint</span></span>](./Remove-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="57bad-165">Set-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="57bad-165">Set-AzureTrafficManagerEndpoint</span></span>](./Set-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="57bad-166">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="57bad-166">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="57bad-167">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="57bad-167">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


