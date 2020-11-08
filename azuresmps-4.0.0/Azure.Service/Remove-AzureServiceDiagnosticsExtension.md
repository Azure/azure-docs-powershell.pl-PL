---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 95298AFC-B492-4EA6-AFC2-E862D3086AF2
online version: ''
schema: 2.0.0
ms.openlocfilehash: f84b1256d7d911d22a4f1344bdf841943ce87ee7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055082"
---
# <span data-ttu-id="be0cf-101">Remove-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="be0cf-101">Remove-AzureServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="be0cf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="be0cf-102">SYNOPSIS</span></span>
<span data-ttu-id="be0cf-103">Usuwa rozszerzenie Diagnostyka usługi w chmurze zastosowane do wszystkich ról lub nazwanych ról w określonym miejscu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="be0cf-103">Removes the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="be0cf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="be0cf-104">SYNTAX</span></span>

### <span data-ttu-id="be0cf-105">RemoveByRoles (domyślny)</span><span class="sxs-lookup"><span data-stu-id="be0cf-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="be0cf-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="be0cf-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [-UninstallConfiguration]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="be0cf-107">Opis</span><span class="sxs-lookup"><span data-stu-id="be0cf-107">DESCRIPTION</span></span>
<span data-ttu-id="be0cf-108">Polecenie cmdlet **Remove-AzureServiceDiagnosticsExtension** usuwa rozszerzenie Diagnostyka usługi w chmurze zastosowane do wszystkich ról lub nazwanych ról w określonym miejscu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="be0cf-108">The **Remove-AzureServiceDiagnosticsExtension** cmdlet removes the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="be0cf-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="be0cf-109">EXAMPLES</span></span>

### <span data-ttu-id="be0cf-110">Przykład 1: Usuwanie rozszerzenia diagnostycznego usługi</span><span class="sxs-lookup"><span data-stu-id="be0cf-110">Example 1: Remove the diagnostic extension for a service</span></span>
```
PS C:\> Remove-AzureServiceDiagnosticsExtension -ServiceName $Svc
```

<span data-ttu-id="be0cf-111">To polecenie usuwa rozszerzenie diagnostyczne dla określonej roli.</span><span class="sxs-lookup"><span data-stu-id="be0cf-111">This command removes the diagnostic extension for a specified role.</span></span>

### <span data-ttu-id="be0cf-112">Przykład 2: Usuwanie rozszerzenia diagnostycznego usługi w określonej roli</span><span class="sxs-lookup"><span data-stu-id="be0cf-112">Example 2: Remove the diagnostic extension for a service in a specified role</span></span>
```
PS C:\> Remove-AzureServiceDiagnosticsExtension -ServiceName $Svc -Role "WebRole01"
```

<span data-ttu-id="be0cf-113">To polecenie usuwa rozszerzenie diagnostyczne dla określonej roli.</span><span class="sxs-lookup"><span data-stu-id="be0cf-113">This command removes the diagnostic extension for a specified role.</span></span>

## <span data-ttu-id="be0cf-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="be0cf-114">PARAMETERS</span></span>

### <span data-ttu-id="be0cf-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="be0cf-115">-InformationAction</span></span>
<span data-ttu-id="be0cf-116">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="be0cf-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="be0cf-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="be0cf-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="be0cf-118">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="be0cf-118">Continue</span></span>
- <span data-ttu-id="be0cf-119">Ignorować</span><span class="sxs-lookup"><span data-stu-id="be0cf-119">Ignore</span></span>
- <span data-ttu-id="be0cf-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="be0cf-120">Inquire</span></span>
- <span data-ttu-id="be0cf-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="be0cf-121">SilentlyContinue</span></span>
- <span data-ttu-id="be0cf-122">Przestaw</span><span class="sxs-lookup"><span data-stu-id="be0cf-122">Stop</span></span>
- <span data-ttu-id="be0cf-123">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="be0cf-123">Suspend</span></span>

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

### <span data-ttu-id="be0cf-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="be0cf-124">-InformationVariable</span></span>
<span data-ttu-id="be0cf-125">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="be0cf-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="be0cf-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="be0cf-126">-Profile</span></span>
<span data-ttu-id="be0cf-127">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be0cf-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="be0cf-128">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="be0cf-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="be0cf-129">-Rola</span><span class="sxs-lookup"><span data-stu-id="be0cf-129">-Role</span></span>
<span data-ttu-id="be0cf-130">Określa opcjonalną tablicę ról, dla których należy określić konfigurację pulpitu zdalnego.</span><span class="sxs-lookup"><span data-stu-id="be0cf-130">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="be0cf-131">Jeśli ten parametr nie zostanie określony, konfiguracja pulpitu zdalnego zostanie zastosowana jako Konfiguracja domyślna dla wszystkich ról.</span><span class="sxs-lookup"><span data-stu-id="be0cf-131">If you do not specify this parameter, the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="be0cf-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="be0cf-132">-ServiceName</span></span>
<span data-ttu-id="be0cf-133">Określa nazwę usługi na platformie Azure wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="be0cf-133">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="be0cf-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="be0cf-134">-Slot</span></span>
<span data-ttu-id="be0cf-135">Określa środowisko wdrożenia, które ma zostać zmodyfikowane.</span><span class="sxs-lookup"><span data-stu-id="be0cf-135">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="be0cf-136">Prawidłowe wartości to Production lub Staging.</span><span class="sxs-lookup"><span data-stu-id="be0cf-136">Valid values are Production or Staging.</span></span>

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

### <span data-ttu-id="be0cf-137">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="be0cf-137">-UninstallConfiguration</span></span>
<span data-ttu-id="be0cf-138">Wskazuje, że to polecenie cmdlet Odinstalowuje wszystkie konfiguracje protokołu RDP z usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="be0cf-138">Indicates that this cmdlet uninstalls all RDP configurations from the cloud service.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveAllRoles
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be0cf-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be0cf-139">CommonParameters</span></span>
<span data-ttu-id="be0cf-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be0cf-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be0cf-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be0cf-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be0cf-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be0cf-142">INPUTS</span></span>

## <span data-ttu-id="be0cf-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="be0cf-143">OUTPUTS</span></span>

## <span data-ttu-id="be0cf-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="be0cf-144">NOTES</span></span>

## <span data-ttu-id="be0cf-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be0cf-145">RELATED LINKS</span></span>

[<span data-ttu-id="be0cf-146">Get-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="be0cf-146">Get-AzureServiceDiagnosticsExtension</span></span>](./Get-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="be0cf-147">Set-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="be0cf-147">Set-AzureServiceDiagnosticsExtension</span></span>](./Set-AzureServiceDiagnosticsExtension.md)


