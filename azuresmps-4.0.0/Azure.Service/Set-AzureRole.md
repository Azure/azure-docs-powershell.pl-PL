---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8170AEF9-46E6-4087-8A68-29DFD5D014B5
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb63d143ca2cafce92109e17fd3ced6a9dc070e8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054790"
---
# <span data-ttu-id="6e2f7-101">Set-AzureRole</span><span class="sxs-lookup"><span data-stu-id="6e2f7-101">Set-AzureRole</span></span>

## <span data-ttu-id="6e2f7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6e2f7-102">SYNOPSIS</span></span>
<span data-ttu-id="6e2f7-103">Ustawia liczbę wystąpień roli platformy Azure do uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="6e2f7-103">Sets the number of instances of an Azure role to run.</span></span>

## <span data-ttu-id="6e2f7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6e2f7-104">SYNTAX</span></span>

```
Set-AzureRole [-ServiceName] <String> [-Slot] <String> [-RoleName] <String> [-Count] <Int32>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="6e2f7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6e2f7-105">DESCRIPTION</span></span>
<span data-ttu-id="6e2f7-106">Polecenie cmdlet **Set-AzureRole** określa liczbę wystąpień określonej roli, które zostaną uruchomione we wdrożeniu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6e2f7-106">The **Set-AzureRole** cmdlet sets the number of instances of a specified role to run in an Azure deployment.</span></span>

## <span data-ttu-id="6e2f7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6e2f7-107">EXAMPLES</span></span>

### <span data-ttu-id="6e2f7-108">1: Ustawianie liczby wystąpień roli</span><span class="sxs-lookup"><span data-stu-id="6e2f7-108">1: Set the number of instances for a role</span></span>
```
PS C:\> Set-AzureRole -ServiceName "MySvc01" -Slot "Production" -RoleName "MyTestRole03" -Count 3
```

<span data-ttu-id="6e2f7-109">To polecenie ustawia rolę MyTestRole03 działającej w produkcji w usłudze MySvc01, aby mieć trzy wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="6e2f7-109">This command sets the MyTestRole03 role that is running in production on the MySvc01 service to have three instances.</span></span>

## <span data-ttu-id="6e2f7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6e2f7-110">PARAMETERS</span></span>

### <span data-ttu-id="6e2f7-111">-Count</span><span class="sxs-lookup"><span data-stu-id="6e2f7-111">-Count</span></span>
<span data-ttu-id="6e2f7-112">Określa liczbę wystąpień roli, które mają zostać uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6e2f7-112">Specifies the number of role instances to run.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e2f7-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6e2f7-113">-InformationAction</span></span>
<span data-ttu-id="6e2f7-114">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="6e2f7-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6e2f7-115">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6e2f7-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6e2f7-116">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="6e2f7-116">Continue</span></span>
- <span data-ttu-id="6e2f7-117">Ignorować</span><span class="sxs-lookup"><span data-stu-id="6e2f7-117">Ignore</span></span>
- <span data-ttu-id="6e2f7-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="6e2f7-118">Inquire</span></span>
- <span data-ttu-id="6e2f7-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6e2f7-119">SilentlyContinue</span></span>
- <span data-ttu-id="6e2f7-120">Przestaw</span><span class="sxs-lookup"><span data-stu-id="6e2f7-120">Stop</span></span>
- <span data-ttu-id="6e2f7-121">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="6e2f7-121">Suspend</span></span>

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

### <span data-ttu-id="6e2f7-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6e2f7-122">-InformationVariable</span></span>
<span data-ttu-id="6e2f7-123">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="6e2f7-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6e2f7-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="6e2f7-124">-Profile</span></span>
<span data-ttu-id="6e2f7-125">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e2f7-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6e2f7-126">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="6e2f7-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6e2f7-127">-Rolename</span><span class="sxs-lookup"><span data-stu-id="6e2f7-127">-RoleName</span></span>
<span data-ttu-id="6e2f7-128">Określa nazwę roli, dla której ma zostać ustawiona liczba wystąpień.</span><span class="sxs-lookup"><span data-stu-id="6e2f7-128">Specifies the name of the role for which to set the number of instances.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e2f7-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6e2f7-129">-ServiceName</span></span>
<span data-ttu-id="6e2f7-130">Określa nazwę usługi platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6e2f7-130">Specifies the name of the Azure service.</span></span>

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

### <span data-ttu-id="6e2f7-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="6e2f7-131">-Slot</span></span>
<span data-ttu-id="6e2f7-132">Określa środowisko wdrażania wdrożenia, które ma zostać zmodyfikowane.</span><span class="sxs-lookup"><span data-stu-id="6e2f7-132">Specifies the deployment environment of the deployment to modify.</span></span>
<span data-ttu-id="6e2f7-133">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6e2f7-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6e2f7-134">BOM</span><span class="sxs-lookup"><span data-stu-id="6e2f7-134">Production</span></span>
- <span data-ttu-id="6e2f7-135">Most</span><span class="sxs-lookup"><span data-stu-id="6e2f7-135">Staging</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e2f7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e2f7-136">CommonParameters</span></span>
<span data-ttu-id="6e2f7-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e2f7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e2f7-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e2f7-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e2f7-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6e2f7-139">INPUTS</span></span>

## <span data-ttu-id="6e2f7-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6e2f7-140">OUTPUTS</span></span>

## <span data-ttu-id="6e2f7-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6e2f7-141">NOTES</span></span>

## <span data-ttu-id="6e2f7-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6e2f7-142">RELATED LINKS</span></span>

[<span data-ttu-id="6e2f7-143">Get-AzureRole</span><span class="sxs-lookup"><span data-stu-id="6e2f7-143">Get-AzureRole</span></span>](./Get-AzureRole.md)


