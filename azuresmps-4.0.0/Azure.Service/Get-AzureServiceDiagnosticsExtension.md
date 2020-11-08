---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 235DD5D7-BE24-4FBE-88E2-40D1943ED155
online version: ''
schema: 2.0.0
ms.openlocfilehash: e4fb3f35bc64a1431550d4da5aa669e934cd3a7f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054569"
---
# <span data-ttu-id="514b9-101">Get-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="514b9-101">Get-AzureServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="514b9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="514b9-102">SYNOPSIS</span></span>
<span data-ttu-id="514b9-103">Pobiera rozszerzenie Diagnostyka usługi w chmurze zastosowane do wszystkich ról lub nazwanych ról w określonym miejscu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="514b9-103">Gets the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="514b9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="514b9-104">SYNTAX</span></span>

```
Get-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="514b9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="514b9-105">DESCRIPTION</span></span>
<span data-ttu-id="514b9-106">Polecenie cmdlet **Get-AzureServiceDiagnosticsExtension** pobiera rozszerzenie Diagnostyka usługi w chmurze zastosowane do wszystkich ról lub nazwanych ról w określonym miejscu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="514b9-106">The **Get-AzureServiceDiagnosticsExtension** cmdlet gets the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="514b9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="514b9-107">EXAMPLES</span></span>

### <span data-ttu-id="514b9-108">Przykład 1: uzyskiwanie rozszerzenia Diagnostyka usługi</span><span class="sxs-lookup"><span data-stu-id="514b9-108">Example 1: Get service diagnostics extension</span></span> 
```
PS C:\> Get-AzureServiceDiagnosticsExtension -ServiceName $Svc
```

<span data-ttu-id="514b9-109">To polecenie uzyskuje program Service Diagnostics dla usługi we wszystkich rolach.</span><span class="sxs-lookup"><span data-stu-id="514b9-109">This command gets the service diagnostics for a service, across all roles.</span></span>

## <span data-ttu-id="514b9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="514b9-110">PARAMETERS</span></span>

### <span data-ttu-id="514b9-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="514b9-111">-InformationAction</span></span>
<span data-ttu-id="514b9-112">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="514b9-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="514b9-113">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="514b9-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="514b9-114">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="514b9-114">Continue</span></span>
- <span data-ttu-id="514b9-115">Ignorować</span><span class="sxs-lookup"><span data-stu-id="514b9-115">Ignore</span></span>
- <span data-ttu-id="514b9-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="514b9-116">Inquire</span></span>
- <span data-ttu-id="514b9-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="514b9-117">SilentlyContinue</span></span>
- <span data-ttu-id="514b9-118">Przestaw</span><span class="sxs-lookup"><span data-stu-id="514b9-118">Stop</span></span>
- <span data-ttu-id="514b9-119">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="514b9-119">Suspend</span></span>

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

### <span data-ttu-id="514b9-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="514b9-120">-InformationVariable</span></span>
<span data-ttu-id="514b9-121">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="514b9-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="514b9-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="514b9-122">-Profile</span></span>
<span data-ttu-id="514b9-123">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="514b9-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="514b9-124">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="514b9-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="514b9-125">-Rola</span><span class="sxs-lookup"><span data-stu-id="514b9-125">-Role</span></span>
<span data-ttu-id="514b9-126">Określa tablicę ról.</span><span class="sxs-lookup"><span data-stu-id="514b9-126">Specifies an array of roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="514b9-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="514b9-127">-ServiceName</span></span>
<span data-ttu-id="514b9-128">Określa nazwę usługi na platformie Azure wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="514b9-128">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="514b9-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="514b9-129">-Slot</span></span>
<span data-ttu-id="514b9-130">Określa środowisko wdrożenia, które ma zostać zmodyfikowane.</span><span class="sxs-lookup"><span data-stu-id="514b9-130">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="514b9-131">Dopuszczalne wartości tego parametru to: production lub Staging.</span><span class="sxs-lookup"><span data-stu-id="514b9-131">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="514b9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="514b9-132">CommonParameters</span></span>
<span data-ttu-id="514b9-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="514b9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="514b9-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="514b9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="514b9-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="514b9-135">INPUTS</span></span>

## <span data-ttu-id="514b9-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="514b9-136">OUTPUTS</span></span>

## <span data-ttu-id="514b9-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="514b9-137">NOTES</span></span>

## <span data-ttu-id="514b9-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="514b9-138">RELATED LINKS</span></span>

[<span data-ttu-id="514b9-139">Remove-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="514b9-139">Remove-AzureServiceDiagnosticsExtension</span></span>](./Remove-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="514b9-140">Set-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="514b9-140">Set-AzureServiceDiagnosticsExtension</span></span>](./Set-AzureServiceDiagnosticsExtension.md)


