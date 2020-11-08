---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6A280C0B-5F55-4575-9B11-596F497C4305
online version: ''
schema: 2.0.0
ms.openlocfilehash: 71e49425724926848ee69b24f5dfca70df664913
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055092"
---
# <span data-ttu-id="fe2ca-101">Remove-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="fe2ca-101">Remove-AzureServiceADDomainExtension</span></span>

## <span data-ttu-id="fe2ca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fe2ca-102">SYNOPSIS</span></span>
<span data-ttu-id="fe2ca-103">Usuwa rozszerzenie domeny usługi w chmurze, stosowane na wszystkich rolach lub nazwanych rolach w określonym miejscu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-103">Removes the cloud service AD domain extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="fe2ca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fe2ca-104">SYNTAX</span></span>

### <span data-ttu-id="fe2ca-105">RemoveByRoles (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fe2ca-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="fe2ca-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="fe2ca-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [-UninstallConfiguration]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="fe2ca-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fe2ca-107">DESCRIPTION</span></span>
<span data-ttu-id="fe2ca-108">Polecenie cmdlet **Remove-AzureServiceADDomainExtension** usuwa rozszerzenie domeny usługi Cloud Active Directory (AD) zastosowane na wszystkich rolach lub nazwanych rolach w określonym miejscu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-108">The **Remove-AzureServiceADDomainExtension** cmdlet removes the cloud service Active Directory (AD) domain extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="fe2ca-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fe2ca-109">EXAMPLES</span></span>

### <span data-ttu-id="fe2ca-110">Przykład 1: Usuwanie rozszerzenia domeny usługi AD</span><span class="sxs-lookup"><span data-stu-id="fe2ca-110">Example 1: Remove an AD domain extension</span></span>
```
PS C:\> Remove-AzureServiceADDomainExtension -ServiceName $Svc
```

<span data-ttu-id="fe2ca-111">To polecenie usuwa rozszerzenie określone przez zmienną $Svc.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-111">This command removes the extension specified by the $Svc variable.</span></span>

### <span data-ttu-id="fe2ca-112">Przykład 2: Usuwanie rozszerzenia domeny usługi Active Directory dla określonej roli</span><span class="sxs-lookup"><span data-stu-id="fe2ca-112">Example 2: Remove an AD Domain extension for a specified role</span></span>
```
PS C:\> Remove-AzureServiceADDomainExtension -ServiceName $Svc -Role "WebRole1"
```

<span data-ttu-id="fe2ca-113">To polecenie usuwa rozszerzenie usługi dla określonej roli.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-113">This command removes the service extension for the specified role.</span></span>

## <span data-ttu-id="fe2ca-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fe2ca-114">PARAMETERS</span></span>

### <span data-ttu-id="fe2ca-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="fe2ca-115">-InformationAction</span></span>
<span data-ttu-id="fe2ca-116">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fe2ca-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="fe2ca-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fe2ca-118">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="fe2ca-118">Continue</span></span>
- <span data-ttu-id="fe2ca-119">Ignorować</span><span class="sxs-lookup"><span data-stu-id="fe2ca-119">Ignore</span></span>
- <span data-ttu-id="fe2ca-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="fe2ca-120">Inquire</span></span>
- <span data-ttu-id="fe2ca-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fe2ca-121">SilentlyContinue</span></span>
- <span data-ttu-id="fe2ca-122">Przestaw</span><span class="sxs-lookup"><span data-stu-id="fe2ca-122">Stop</span></span>
- <span data-ttu-id="fe2ca-123">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="fe2ca-123">Suspend</span></span>

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

### <span data-ttu-id="fe2ca-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fe2ca-124">-InformationVariable</span></span>
<span data-ttu-id="fe2ca-125">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fe2ca-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="fe2ca-126">-Profile</span></span>
<span data-ttu-id="fe2ca-127">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fe2ca-128">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fe2ca-129">-Rola</span><span class="sxs-lookup"><span data-stu-id="fe2ca-129">-Role</span></span>
<span data-ttu-id="fe2ca-130">Określa opcjonalną tablicę ról, dla których należy określić konfigurację pulpitu zdalnego.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-130">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="fe2ca-131">Jeśli nie określono tej reguły, konfiguracja domeny usługi AD zostanie zastosowana jako Konfiguracja domyślna dla wszystkich ról.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-131">If not specified, the AD domain configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="fe2ca-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="fe2ca-132">-ServiceName</span></span>
<span data-ttu-id="fe2ca-133">Określa nazwę usługi platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-133">Specifies the name of an Azure service.</span></span>

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

### <span data-ttu-id="fe2ca-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="fe2ca-134">-Slot</span></span>
<span data-ttu-id="fe2ca-135">Określa środowisko wdrożenia, które ma zostać zmodyfikowane.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-135">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="fe2ca-136">Prawidłowe wartości to: production lub Staging.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-136">Valid values are: Production or Staging.</span></span>

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

### <span data-ttu-id="fe2ca-137">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe2ca-137">-UninstallConfiguration</span></span>
<span data-ttu-id="fe2ca-138">Wskazuje, że to polecenie cmdlet Odinstalowuje wszystkie konfiguracje domeny usługi Active Directory z usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-138">Indicates that this cmdlet uninstalls all AD domain configurations from the cloud service.</span></span>

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

### <span data-ttu-id="fe2ca-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe2ca-139">CommonParameters</span></span>
<span data-ttu-id="fe2ca-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe2ca-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe2ca-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe2ca-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe2ca-142">INPUTS</span></span>

## <span data-ttu-id="fe2ca-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fe2ca-143">OUTPUTS</span></span>

## <span data-ttu-id="fe2ca-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fe2ca-144">NOTES</span></span>

## <span data-ttu-id="fe2ca-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe2ca-145">RELATED LINKS</span></span>

[<span data-ttu-id="fe2ca-146">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="fe2ca-146">Get-AzureServiceADDomainExtension</span></span>](./Get-AzureServiceADDomainExtension.md)

[<span data-ttu-id="fe2ca-147">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="fe2ca-147">Set-AzureServiceADDomainExtension</span></span>](./Set-AzureServiceADDomainExtension.md)


