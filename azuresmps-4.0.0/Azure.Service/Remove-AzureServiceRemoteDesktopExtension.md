---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C263CCAD-E51F-420E-9AD4-4FAC09C99CB1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3c10a7694034fe4400ed415891e74f7089ce8558
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055078"
---
# <span data-ttu-id="5a99f-101">Remove-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="5a99f-101">Remove-AzureServiceRemoteDesktopExtension</span></span>

## <span data-ttu-id="5a99f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5a99f-102">SYNOPSIS</span></span>
<span data-ttu-id="5a99f-103">Usuwa rozszerzenie pulpitu zdalnego usługi w chmurze zastosowane do wszystkich ról lub nazwanych ról w określonym miejscu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="5a99f-103">Removes the cloud service remote desktop extension applied on all roles or named roles at a specified deployment slot.</span></span>

## <span data-ttu-id="5a99f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5a99f-104">SYNTAX</span></span>

### <span data-ttu-id="5a99f-105">RemoveByRoles (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5a99f-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="5a99f-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="5a99f-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>]
 [-UninstallConfiguration] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5a99f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5a99f-107">DESCRIPTION</span></span>
<span data-ttu-id="5a99f-108">Polecenie cmdlet **Remove-AzureServiceRemoteDesktopExtension** usuwa rozszerzenie pulpitu zdalnego usługi w chmurze zastosowane do wszystkich ról lub nazwanych ról w określonym miejscu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="5a99f-108">The **Remove-AzureServiceRemoteDesktopExtension** cmdlet removes the cloud service remote desktop extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="5a99f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5a99f-109">EXAMPLES</span></span>

### <span data-ttu-id="5a99f-110">Przykład 1: Usuwanie rozszerzenia pulpitu zdalnego</span><span class="sxs-lookup"><span data-stu-id="5a99f-110">Example 1: Remove the remote desktop extension</span></span>
```
PS C:\> Remove-AzureServiceRemoteDesktopExtension -ServiceName $svc
```

<span data-ttu-id="5a99f-111">To polecenie usuwa rozszerzenie pulpitu zdalnego.</span><span class="sxs-lookup"><span data-stu-id="5a99f-111">This command removes the remote desktop extension.</span></span>

### <span data-ttu-id="5a99f-112">Przykład 2: Usuwanie rozszerzenia pulpitu zdalnego z określonej roli</span><span class="sxs-lookup"><span data-stu-id="5a99f-112">Example 2: Remove the remote desktop extension from a specified role</span></span>
```
PS C:\> Remove-AzureServiceRemoteDesktopExtension -ServiceName $svc -Role "WebRole1"
```

<span data-ttu-id="5a99f-113">To polecenie usuwa rozszerzenie pulpitu zdalnego z określonej roli.</span><span class="sxs-lookup"><span data-stu-id="5a99f-113">This command removes the remote desktop extension from a specified role.</span></span>

## <span data-ttu-id="5a99f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5a99f-114">PARAMETERS</span></span>

### <span data-ttu-id="5a99f-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5a99f-115">-InformationAction</span></span>
<span data-ttu-id="5a99f-116">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="5a99f-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5a99f-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5a99f-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5a99f-118">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="5a99f-118">Continue</span></span>
- <span data-ttu-id="5a99f-119">Ignorować</span><span class="sxs-lookup"><span data-stu-id="5a99f-119">Ignore</span></span>
- <span data-ttu-id="5a99f-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="5a99f-120">Inquire</span></span>
- <span data-ttu-id="5a99f-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5a99f-121">SilentlyContinue</span></span>
- <span data-ttu-id="5a99f-122">Przestaw</span><span class="sxs-lookup"><span data-stu-id="5a99f-122">Stop</span></span>
- <span data-ttu-id="5a99f-123">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="5a99f-123">Suspend</span></span>

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

### <span data-ttu-id="5a99f-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5a99f-124">-InformationVariable</span></span>
<span data-ttu-id="5a99f-125">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="5a99f-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5a99f-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="5a99f-126">-Profile</span></span>
<span data-ttu-id="5a99f-127">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a99f-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5a99f-128">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="5a99f-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5a99f-129">-Rola</span><span class="sxs-lookup"><span data-stu-id="5a99f-129">-Role</span></span>
<span data-ttu-id="5a99f-130">Określa opcjonalną tablicę ról określającą konfigurację pulpitu zdalnego.</span><span class="sxs-lookup"><span data-stu-id="5a99f-130">Specifies an optional array of roles to specify the remote desktop configuration for.</span></span>
<span data-ttu-id="5a99f-131">Jeśli nie określono, konfiguracja pulpitu zdalnego jest stosowana jako Konfiguracja domyślna dla wszystkich ról.</span><span class="sxs-lookup"><span data-stu-id="5a99f-131">If not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="5a99f-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5a99f-132">-ServiceName</span></span>
<span data-ttu-id="5a99f-133">Określa nazwę usługi na platformie Azure wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="5a99f-133">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="5a99f-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="5a99f-134">-Slot</span></span>
<span data-ttu-id="5a99f-135">Określa środowisko wdrożenia, które ma zostać zmodyfikowane.</span><span class="sxs-lookup"><span data-stu-id="5a99f-135">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="5a99f-136">Obsługiwane wartości to "produkcja" lub "przemieszczanie".</span><span class="sxs-lookup"><span data-stu-id="5a99f-136">Supported values are "Production" or "Staging".</span></span>

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

### <span data-ttu-id="5a99f-137">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a99f-137">-UninstallConfiguration</span></span>
<span data-ttu-id="5a99f-138">Określa, że to polecenie cmdlet Odinstalowuje wszystkie konfiguracje protokołu RDP z usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="5a99f-138">Specifies that this cmdlet uninstalls all RDP configurations from the cloud service.</span></span>

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

### <span data-ttu-id="5a99f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a99f-139">CommonParameters</span></span>
<span data-ttu-id="5a99f-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a99f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a99f-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a99f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a99f-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a99f-142">INPUTS</span></span>

## <span data-ttu-id="5a99f-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5a99f-143">OUTPUTS</span></span>

## <span data-ttu-id="5a99f-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5a99f-144">NOTES</span></span>

## <span data-ttu-id="5a99f-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a99f-145">RELATED LINKS</span></span>

[<span data-ttu-id="5a99f-146">Set-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="5a99f-146">Set-AzureServiceRemoteDesktopExtension</span></span>](./Set-AzureServiceRemoteDesktopExtension.md)


