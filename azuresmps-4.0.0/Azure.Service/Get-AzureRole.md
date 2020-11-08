---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7C50472E-CE36-4BF1-92C9-A3B9B183ACD1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 929b439c58c344a1902c497bbad6e056e3755025
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055280"
---
# <span data-ttu-id="2bb89-101">Get-AzureRole</span><span class="sxs-lookup"><span data-stu-id="2bb89-101">Get-AzureRole</span></span>

## <span data-ttu-id="2bb89-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2bb89-102">SYNOPSIS</span></span>
<span data-ttu-id="2bb89-103">Zwraca listę ról w usłudze Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2bb89-103">Returns a list of roles in your Microsoft Azure service.</span></span>

## <span data-ttu-id="2bb89-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2bb89-104">SYNTAX</span></span>

```
Get-AzureRole [-ServiceName] <String> [[-Slot] <String>] [[-RoleName] <String>] [-InstanceDetails]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="2bb89-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2bb89-105">DESCRIPTION</span></span>
<span data-ttu-id="2bb89-106">Polecenie cmdlet **Get-AzureRole** zwraca obiekt listy ze szczegółami dotyczącymi ról w usłudze Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2bb89-106">The **Get-AzureRole** cmdlet returns a list object with details on the roles in your Microsoft Azure service.</span></span>
<span data-ttu-id="2bb89-107">Jeśli określisz parametr *rolename* , funkcja **Get-AzureRole** zwraca dane tylko w ramach tej roli.</span><span class="sxs-lookup"><span data-stu-id="2bb89-107">If you specify the *RoleName* parameter, **Get-AzureRole** returns details on that role only.</span></span>
<span data-ttu-id="2bb89-108">Jeśli określisz parametr *InstanceDetails* , zostaną zwrócone dodatkowe szczegóły dotyczące wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="2bb89-108">If you specify the *InstanceDetails* parameter, additional, instance-specific details are returned.</span></span>

## <span data-ttu-id="2bb89-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2bb89-109">EXAMPLES</span></span>

### <span data-ttu-id="2bb89-110">Przykład 1: uzyskiwanie listy ról dla usługi</span><span class="sxs-lookup"><span data-stu-id="2bb89-110">Example 1: Get a list of roles for a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production"
```

<span data-ttu-id="2bb89-111">To polecenie zwraca obiekt ze szczegółami dotyczącymi wszystkich ról produkcyjnych uruchomionych w usłudze MySvc01.</span><span class="sxs-lookup"><span data-stu-id="2bb89-111">This command returns an object with details on all the production roles running on the MySvc01 service.</span></span>

### <span data-ttu-id="2bb89-112">Przykład 2: uzyskiwanie szczegółowych informacji na temat roli działającej w usłudze</span><span class="sxs-lookup"><span data-stu-id="2bb89-112">Example 2: Get details on a role running on a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc1" -Slot "Staging" -RoleName "MyTestVM3"
```

<span data-ttu-id="2bb89-113">To polecenie zwraca obiekt ze szczegółami dotyczącymi roli MyTestVM3, działając w środowisku przemieszczania usługi MySvc01.</span><span class="sxs-lookup"><span data-stu-id="2bb89-113">This command returns an object with details on the MyTestVM3 role, running on the staging environment of the MySvc01 service.</span></span>

### <span data-ttu-id="2bb89-114">Przykład 3: uzyskiwanie informacji o wystąpieniu dla wystąpień roli uruchomionych w usłudze</span><span class="sxs-lookup"><span data-stu-id="2bb89-114">Example 3: Get instance information on instances of a role running on a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production" -RoleName "MyTestVM02" -InstanceDetails
```

<span data-ttu-id="2bb89-115">To polecenie zwraca obiekt ze szczegółami dotyczącymi wystąpień roli MyTestVM02 działającej w środowisku produkcyjnym w usłudze MySvc01.</span><span class="sxs-lookup"><span data-stu-id="2bb89-115">This command returns an object with details on the instances of the MyTestVM02 role running in the production environment on the MySvc01 service.</span></span>

### <span data-ttu-id="2bb89-116">Przykład 4: uzyskiwanie tabeli wystąpień ról skojarzonych z usługą</span><span class="sxs-lookup"><span data-stu-id="2bb89-116">Example 4: Get a table of the role instances associated with a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production" -InstanceDetails | Format-Table -Auto "InstanceName", "InstanceSize", "InstanceStatus"
```

<span data-ttu-id="2bb89-117">To polecenie zwraca tabelę z nazwą wystąpienia, rozmiarem i stanem wszystkich wystąpień ról uruchomionych w środowisku produkcyjnym w usłudze MySvc01.</span><span class="sxs-lookup"><span data-stu-id="2bb89-117">This command returns a table of the instance name, size, and status of all role instances running in the production environment on the MySvc01 service.</span></span>

## <span data-ttu-id="2bb89-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2bb89-118">PARAMETERS</span></span>

### <span data-ttu-id="2bb89-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2bb89-119">-InformationAction</span></span>
<span data-ttu-id="2bb89-120">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="2bb89-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2bb89-121">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="2bb89-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2bb89-122">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="2bb89-122">Continue</span></span>
- <span data-ttu-id="2bb89-123">Ignorować</span><span class="sxs-lookup"><span data-stu-id="2bb89-123">Ignore</span></span>
- <span data-ttu-id="2bb89-124">Inquire</span><span class="sxs-lookup"><span data-stu-id="2bb89-124">Inquire</span></span>
- <span data-ttu-id="2bb89-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2bb89-125">SilentlyContinue</span></span>
- <span data-ttu-id="2bb89-126">Przestaw</span><span class="sxs-lookup"><span data-stu-id="2bb89-126">Stop</span></span>
- <span data-ttu-id="2bb89-127">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="2bb89-127">Suspend</span></span>

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

### <span data-ttu-id="2bb89-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2bb89-128">-InformationVariable</span></span>
<span data-ttu-id="2bb89-129">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="2bb89-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2bb89-130">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="2bb89-130">-InstanceDetails</span></span>
<span data-ttu-id="2bb89-131">Określa, że to polecenie cmdlet zwraca szczegóły dotyczące wystąpień poszczególnych ról.</span><span class="sxs-lookup"><span data-stu-id="2bb89-131">Specifies that this cmdlet returns details about the instances on each role.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bb89-132">-Profile</span><span class="sxs-lookup"><span data-stu-id="2bb89-132">-Profile</span></span>
<span data-ttu-id="2bb89-133">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bb89-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2bb89-134">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="2bb89-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2bb89-135">-Rolename</span><span class="sxs-lookup"><span data-stu-id="2bb89-135">-RoleName</span></span>
<span data-ttu-id="2bb89-136">Określa nazwę roli, którą należy uzyskać.</span><span class="sxs-lookup"><span data-stu-id="2bb89-136">Specifies the name of the role to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bb89-137">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2bb89-137">-ServiceName</span></span>
<span data-ttu-id="2bb89-138">Określa nazwę usługi platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2bb89-138">Specifies the name of the Azure service.</span></span>

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

### <span data-ttu-id="2bb89-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="2bb89-139">-Slot</span></span>
<span data-ttu-id="2bb89-140">Określa środowisko wdrażania platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2bb89-140">Specifies the Azure deployment environment.</span></span>
<span data-ttu-id="2bb89-141">Dopuszczalne wartości tego parametru to: production lub Staging.</span><span class="sxs-lookup"><span data-stu-id="2bb89-141">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="2bb89-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bb89-142">CommonParameters</span></span>
<span data-ttu-id="2bb89-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bb89-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bb89-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bb89-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bb89-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2bb89-145">INPUTS</span></span>

## <span data-ttu-id="2bb89-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2bb89-146">OUTPUTS</span></span>

## <span data-ttu-id="2bb89-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2bb89-147">NOTES</span></span>

## <span data-ttu-id="2bb89-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2bb89-148">RELATED LINKS</span></span>

[<span data-ttu-id="2bb89-149">Set-AzureRole</span><span class="sxs-lookup"><span data-stu-id="2bb89-149">Set-AzureRole</span></span>](./Set-AzureRole.md)


