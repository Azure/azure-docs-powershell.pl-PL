---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2AEA385F-E180-4564-A62A-9E913C665801
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1fff3ea97c51ee5597e585f3275b25e513c22008
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054446"
---
# <span data-ttu-id="4cd92-101">Reset-AzureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="4cd92-101">Reset-AzureRoleInstance</span></span>

## <span data-ttu-id="4cd92-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4cd92-102">SYNOPSIS</span></span>
<span data-ttu-id="4cd92-103">Żąda ponownego uruchomienia lub odobrazowania pojedynczego wystąpienia roli lub wszystkich wystąpień ról określonej roli.</span><span class="sxs-lookup"><span data-stu-id="4cd92-103">Requests a reboot or reimage of a single role instance or all role instances of a specific role.</span></span>

## <span data-ttu-id="4cd92-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4cd92-104">SYNTAX</span></span>

```
Reset-AzureRoleInstance [-ServiceName] <String> -Slot <String> -InstanceName <String> [-Reboot] [-Reimage]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="4cd92-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4cd92-105">DESCRIPTION</span></span>
<span data-ttu-id="4cd92-106">Polecenie cmdlet **Reseting-AzureRoleInstance** żąda ponownego uruchomienia lub ponownego obrazu wystąpienia roli uruchomionego we wdrożeniu.</span><span class="sxs-lookup"><span data-stu-id="4cd92-106">The **Reset-AzureRoleInstance** cmdlet requests a reboot or a reimage of a role instance that is running in a deployment.</span></span>
<span data-ttu-id="4cd92-107">Ta operacja jest wykonywana synchronicznie.</span><span class="sxs-lookup"><span data-stu-id="4cd92-107">This operation executes synchronously.</span></span>
<span data-ttu-id="4cd92-108">Po ponownym uruchomieniu wystąpienia roli usługa Azure przejmuje wystąpienie w trybie offline, ponownie uruchamia system operacyjny dla tego wystąpienia i przełącza wystąpienie z powrotem do trybu online.</span><span class="sxs-lookup"><span data-stu-id="4cd92-108">When you reboot a role instance, Azure takes the instance offline, restarts the underlying operating system for that instance, and brings the instance back online.</span></span>
<span data-ttu-id="4cd92-109">Wszystkie dane zapisywane na dysku lokalnym są zachowywane po ponownym uruchomieniu komputera.</span><span class="sxs-lookup"><span data-stu-id="4cd92-109">Any data that is written to the local disk persists across reboots.</span></span>
<span data-ttu-id="4cd92-110">Wszystkie dane, które są w pamięci, zostaną utracone.</span><span class="sxs-lookup"><span data-stu-id="4cd92-110">Any data that is in-memory is lost.</span></span>

<span data-ttu-id="4cd92-111">Przetworzenie obrazów wystąpienia roli powoduje różne zachowanie w zależności od typu roli.</span><span class="sxs-lookup"><span data-stu-id="4cd92-111">Reimaging a role instance results in different behavior depending on the type of role.</span></span>
<span data-ttu-id="4cd92-112">W przypadku roli sieci Web lub procesu roboczego po zakończeniu działania tej roli usługa Azure przełącza tę rolę do trybu offline i zapisuje nową instalację systemu operacyjnego gościa platformy Azure na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4cd92-112">For a web or worker role, when the role is reimaged, Azure takes the role offline and writes a fresh installation of the Azure guest operating system to the virtual machine.</span></span>
<span data-ttu-id="4cd92-113">Następnie rola jest przywracana w trybie online.</span><span class="sxs-lookup"><span data-stu-id="4cd92-113">The role is then brought back online.</span></span>
<span data-ttu-id="4cd92-114">W przypadku roli maszyny wirtualnej, gdy rola zostanie ponownie utworzona, usługa Azure przełączy tę rolę w tryb offline, ponownie zastosuje obraz niestandardowy, który został przez Ciebie dostarczony, oraz przywraca tę rolę w trybie online.</span><span class="sxs-lookup"><span data-stu-id="4cd92-114">For a VM role, when the role is reimaged, Azure takes the role offline, reapplies the custom image that you provided for it, and brings the role back online.</span></span>

<span data-ttu-id="4cd92-115">Usługa Azure próbuje zachować dane w zasobach magazynu lokalnego, gdy rola zostanie przechowana. Jednak w przypadku przejściowego błędu sprzętowego zasób lokalnego magazynu może zostać utracony.</span><span class="sxs-lookup"><span data-stu-id="4cd92-115">Azure attempts to maintain data in any local storage resources when the role is reimaged; however, in case of a transient hardware failure, the local storage resource may be lost.</span></span>
<span data-ttu-id="4cd92-116">Jeśli aplikacja wymaga zachowywania danych, zalecane jest zapisywanie do trwałego źródła danych, takiego jak dysk Azure.</span><span class="sxs-lookup"><span data-stu-id="4cd92-116">If your application requires that data persist, writing to a durable data source, such as an Azure drive, is recommended.</span></span>
<span data-ttu-id="4cd92-117">Wszystkie dane, które są zapisywane w katalogu lokalnym innym niż zdefiniowany przez zasób lokalnego magazynu, zostaną utracone po przekroczeniu roli.</span><span class="sxs-lookup"><span data-stu-id="4cd92-117">Any data that is written to a local directory other than that defined by the local storage resource will be lost when the role is reimaged.</span></span>

## <span data-ttu-id="4cd92-118">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4cd92-118">EXAMPLES</span></span>

### <span data-ttu-id="4cd92-119">Przykład 1: Ponowna rozruch wystąpienia roli</span><span class="sxs-lookup"><span data-stu-id="4cd92-119">Example 1: Reboot a role instance</span></span>
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -InstanceName "MyWebRole_IN_0" -Reboot
```

<span data-ttu-id="4cd92-120">To polecenie powoduje ponowne uruchomienie wystąpienia roli o nazwie MyWebRole_IN_0 w rozmieszczeniu przemieszczania usługi MySvc01.</span><span class="sxs-lookup"><span data-stu-id="4cd92-120">This command reboots the role instance named MyWebRole_IN_0 in the staging deployment of the MySvc01 service.</span></span>

### <span data-ttu-id="4cd92-121">Przykład 2: rezdjęcie wystąpienia roli</span><span class="sxs-lookup"><span data-stu-id="4cd92-121">Example 2: Reimage a role instance</span></span>
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -Reimage
```

<span data-ttu-id="4cd92-122">To polecenie powoduje ponowne zdjęcie wystąpień roli w ramach przemieszczania usługi w chmurze MySvc01.</span><span class="sxs-lookup"><span data-stu-id="4cd92-122">This command reimages the role instances in the staging deployment of the MySvc01 cloud service.</span></span>

### <span data-ttu-id="4cd92-123">Przykład 3: odobrazowanie wszystkich wystąpień ról</span><span class="sxs-lookup"><span data-stu-id="4cd92-123">Example 3: Reimage all role instances</span></span>
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc1" -Slot "Production" -Reimage
```

<span data-ttu-id="4cd92-124">To polecenie powoduje ponowne zdjęcie wszystkich wystąpień ról we wdrożeniu produkcji usługi MySvc01.</span><span class="sxs-lookup"><span data-stu-id="4cd92-124">This command reimages all role instances in the production deployment of the MySvc01 service.</span></span>

## <span data-ttu-id="4cd92-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4cd92-125">PARAMETERS</span></span>

### <span data-ttu-id="4cd92-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4cd92-126">-InformationAction</span></span>
<span data-ttu-id="4cd92-127">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="4cd92-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4cd92-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="4cd92-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4cd92-129">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="4cd92-129">Continue</span></span>
- <span data-ttu-id="4cd92-130">Ignorować</span><span class="sxs-lookup"><span data-stu-id="4cd92-130">Ignore</span></span>
- <span data-ttu-id="4cd92-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="4cd92-131">Inquire</span></span>
- <span data-ttu-id="4cd92-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4cd92-132">SilentlyContinue</span></span>
- <span data-ttu-id="4cd92-133">Przestaw</span><span class="sxs-lookup"><span data-stu-id="4cd92-133">Stop</span></span>
- <span data-ttu-id="4cd92-134">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="4cd92-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cd92-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4cd92-135">-InformationVariable</span></span>
<span data-ttu-id="4cd92-136">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="4cd92-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cd92-137">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="4cd92-137">-InstanceName</span></span>
<span data-ttu-id="4cd92-138">Określa nazwę wystąpienia roli, które ma być ponownie podobrazem lub ponownym uruchomieniem.</span><span class="sxs-lookup"><span data-stu-id="4cd92-138">Specifies the name of the role instance to reimage or reboot.</span></span>

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

### <span data-ttu-id="4cd92-139">-Profile</span><span class="sxs-lookup"><span data-stu-id="4cd92-139">-Profile</span></span>
<span data-ttu-id="4cd92-140">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cd92-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4cd92-141">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="4cd92-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4cd92-142">-Ponowne uruchamianie</span><span class="sxs-lookup"><span data-stu-id="4cd92-142">-Reboot</span></span>
<span data-ttu-id="4cd92-143">Określa, że to polecenie cmdlet powoduje ponowne uruchomienie określonego wystąpienia roli lub, jeśli nie jest określone, wszystkie wystąpienia ról.</span><span class="sxs-lookup"><span data-stu-id="4cd92-143">Specifies that this cmdlet reboots the specified role instance or, if none is specified, all role instances.</span></span>
<span data-ttu-id="4cd92-144">Musisz dodać parametr *ponownego rozruchu* lub ponownie *obrazu* , ale nie oba.</span><span class="sxs-lookup"><span data-stu-id="4cd92-144">You must include either a *Reboot* or *Reimage* parameter, but not both.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cd92-145">-Reimage</span><span class="sxs-lookup"><span data-stu-id="4cd92-145">-Reimage</span></span>
<span data-ttu-id="4cd92-146">Określa, że to polecenie cmdlet odnosi się do określonego wystąpienia roli lub jeśli nie określono żadnego wystąpienia roli.</span><span class="sxs-lookup"><span data-stu-id="4cd92-146">Specifies that this cmdlet reimages the specified role instance or, if none is specified, all role instances.</span></span>
<span data-ttu-id="4cd92-147">Musisz dodać parametr *ponownego rozruchu* lub ponownie *obrazu* , ale nie oba.</span><span class="sxs-lookup"><span data-stu-id="4cd92-147">You must include either a *Reboot* or *Reimage* parameter, but not both.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cd92-148">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4cd92-148">-ServiceName</span></span>
<span data-ttu-id="4cd92-149">Określa nazwę usługi.</span><span class="sxs-lookup"><span data-stu-id="4cd92-149">Specifies the name of the service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cd92-150">-Slot</span><span class="sxs-lookup"><span data-stu-id="4cd92-150">-Slot</span></span>
<span data-ttu-id="4cd92-151">Określa środowisko wdrażania, w którym są uruchamiane wystąpienia roli.</span><span class="sxs-lookup"><span data-stu-id="4cd92-151">Specifies the deployment environment where the role instances run.</span></span>
<span data-ttu-id="4cd92-152">Prawidłowe wartości: produkcja i przemieszczanie.</span><span class="sxs-lookup"><span data-stu-id="4cd92-152">Valid values are: Production and Staging.</span></span>
<span data-ttu-id="4cd92-153">Możesz dodać parametr *deploymentname* lub *slot* , ale nie oba.</span><span class="sxs-lookup"><span data-stu-id="4cd92-153">You can include either the *DeploymentName* or *Slot* parameter, but not both.</span></span>

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

### <span data-ttu-id="4cd92-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cd92-154">CommonParameters</span></span>
<span data-ttu-id="4cd92-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cd92-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cd92-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cd92-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cd92-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4cd92-157">INPUTS</span></span>

## <span data-ttu-id="4cd92-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4cd92-158">OUTPUTS</span></span>

## <span data-ttu-id="4cd92-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4cd92-159">NOTES</span></span>

## <span data-ttu-id="4cd92-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4cd92-160">RELATED LINKS</span></span>

[<span data-ttu-id="4cd92-161">Set-AzureRole</span><span class="sxs-lookup"><span data-stu-id="4cd92-161">Set-AzureRole</span></span>](./Set-AzureRole.md)


