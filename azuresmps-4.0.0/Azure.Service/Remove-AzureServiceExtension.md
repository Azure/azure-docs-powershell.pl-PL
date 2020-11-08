---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6B5E4968-5DF5-4956-A070-9F54A79D960B
online version: ''
schema: 2.0.0
ms.openlocfilehash: f45e0a93b2f6261ca6031aa721bda3a72f4443dd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055079"
---
# <span data-ttu-id="ff240-101">Remove-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="ff240-101">Remove-AzureServiceExtension</span></span>

## <span data-ttu-id="ff240-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ff240-102">SYNOPSIS</span></span>
<span data-ttu-id="ff240-103">Usuwa rozszerzenia usługi w chmurze zastosowane do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ff240-103">Removes cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="ff240-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ff240-104">SYNTAX</span></span>

### <span data-ttu-id="ff240-105">RemoveByRoles (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ff240-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-ExtensionName] <String> [-ProviderNamespace] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ff240-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="ff240-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [-ExtensionName] <String>
 [-ProviderNamespace] <String> [-UninstallConfiguration] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ff240-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ff240-107">DESCRIPTION</span></span>
<span data-ttu-id="ff240-108">Polecenie cmdlet **Remove-AzureServiceExtension** usuwa rozszerzenia usługi w chmurze zastosowane do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ff240-108">The **Remove-AzureServiceExtension** cmdlet removes cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="ff240-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ff240-109">EXAMPLES</span></span>

### <span data-ttu-id="ff240-110">Przykład 1: Usuwanie rozszerzenia usługi</span><span class="sxs-lookup"><span data-stu-id="ff240-110">Example 1: Remove a service extension</span></span>
```
PS C:\> Remove-AzureServiceExtension -ServiceName $Svc -Slot "Production" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions"
```

<span data-ttu-id="ff240-111">To polecenie usuwa rozszerzenie usługi.</span><span class="sxs-lookup"><span data-stu-id="ff240-111">This command removes a service extension.</span></span>

### <span data-ttu-id="ff240-112">Przykład 2: Usuwanie rozszerzenia usługi i odinstalowywanie wszystkich konfiguracji</span><span class="sxs-lookup"><span data-stu-id="ff240-112">Example 2: Remove a service extension and uninstall all configurations</span></span>
```
PS C:\> Remove-AzureServiceExtension -ServiceName $Svc -Slot "Production" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions" -UninstallConfiguration
```

<span data-ttu-id="ff240-113">To polecenie usuwa rozszerzenie usługi i odinstalowuje wszystkie konfiguracje.</span><span class="sxs-lookup"><span data-stu-id="ff240-113">This command removes a service extension and uninstalls all configurations.</span></span>

## <span data-ttu-id="ff240-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ff240-114">PARAMETERS</span></span>

### <span data-ttu-id="ff240-115">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="ff240-115">-ExtensionName</span></span>
<span data-ttu-id="ff240-116">Określa nazwę rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="ff240-116">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff240-117">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ff240-117">-InformationAction</span></span>
<span data-ttu-id="ff240-118">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="ff240-118">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ff240-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ff240-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ff240-120">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="ff240-120">Continue</span></span>
- <span data-ttu-id="ff240-121">Ignorować</span><span class="sxs-lookup"><span data-stu-id="ff240-121">Ignore</span></span>
- <span data-ttu-id="ff240-122">Inquire</span><span class="sxs-lookup"><span data-stu-id="ff240-122">Inquire</span></span>
- <span data-ttu-id="ff240-123">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ff240-123">SilentlyContinue</span></span>
- <span data-ttu-id="ff240-124">Przestaw</span><span class="sxs-lookup"><span data-stu-id="ff240-124">Stop</span></span>
- <span data-ttu-id="ff240-125">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="ff240-125">Suspend</span></span>

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

### <span data-ttu-id="ff240-126">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ff240-126">-InformationVariable</span></span>
<span data-ttu-id="ff240-127">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="ff240-127">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ff240-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="ff240-128">-Profile</span></span>
<span data-ttu-id="ff240-129">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff240-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ff240-130">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="ff240-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ff240-131">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="ff240-131">-ProviderNamespace</span></span>
<span data-ttu-id="ff240-132">Określa obszar nazw dostawcy rozszerzeń.</span><span class="sxs-lookup"><span data-stu-id="ff240-132">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff240-133">-Rola</span><span class="sxs-lookup"><span data-stu-id="ff240-133">-Role</span></span>
<span data-ttu-id="ff240-134">Określa opcjonalną tablicę ról określającą rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="ff240-134">Specifies an optional array of roles to specify the extension for.</span></span>
<span data-ttu-id="ff240-135">Jeśli nie określono, rozszerzenie jest stosowane jako Konfiguracja domyślna dla wszystkich ról.</span><span class="sxs-lookup"><span data-stu-id="ff240-135">If not specified the extension is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: RemoveByRoles
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff240-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ff240-136">-ServiceName</span></span>
<span data-ttu-id="ff240-137">Określa nazwę usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="ff240-137">Specifies the cloud service name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff240-138">-Slot</span><span class="sxs-lookup"><span data-stu-id="ff240-138">-Slot</span></span>
<span data-ttu-id="ff240-139">Określa środowisko wdrożenia, które ma zostać zmodyfikowane.</span><span class="sxs-lookup"><span data-stu-id="ff240-139">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="ff240-140">Prawidłowe wartości to Production lub Staging.</span><span class="sxs-lookup"><span data-stu-id="ff240-140">Valid values are Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff240-141">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff240-141">-UninstallConfiguration</span></span>
<span data-ttu-id="ff240-142">Wskazuje, że to polecenie cmdlet Odinstalowuje wszystkie konfiguracje z usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="ff240-142">Indicates that this cmdlet uninstalls all configurations from the cloud service.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveAllRoles
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff240-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff240-143">CommonParameters</span></span>
<span data-ttu-id="ff240-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff240-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff240-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff240-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff240-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff240-146">INPUTS</span></span>

## <span data-ttu-id="ff240-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ff240-147">OUTPUTS</span></span>

## <span data-ttu-id="ff240-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ff240-148">NOTES</span></span>

## <span data-ttu-id="ff240-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ff240-149">RELATED LINKS</span></span>

[<span data-ttu-id="ff240-150">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="ff240-150">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)

[<span data-ttu-id="ff240-151">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="ff240-151">Set-AzureServiceExtension</span></span>](./Set-AzureServiceExtension.md)


