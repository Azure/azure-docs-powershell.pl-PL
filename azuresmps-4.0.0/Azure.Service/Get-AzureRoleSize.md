---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2CBF8DEF-954C-4D9F-B495-C2F76550BC79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35f7e8a7a08ac2793b7e4aeb8615e5fb8fc1f727
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054581"
---
# <span data-ttu-id="aac3c-101">Get-AzureRoleSize</span><span class="sxs-lookup"><span data-stu-id="aac3c-101">Get-AzureRoleSize</span></span>

## <span data-ttu-id="aac3c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aac3c-102">SYNOPSIS</span></span>
<span data-ttu-id="aac3c-103">Pobiera informacje o rozmiarze roli dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="aac3c-103">Gets the role size information for the current subscription.</span></span>

## <span data-ttu-id="aac3c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aac3c-104">SYNTAX</span></span>

```
Get-AzureRoleSize [[-InstanceSize] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="aac3c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="aac3c-105">DESCRIPTION</span></span>
<span data-ttu-id="aac3c-106">Polecenie cmdlet **Get-AzureRoleSize** pobiera informacje o rozmiarze roli dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="aac3c-106">The **Get-AzureRoleSize** cmdlet gets the role size information for the current subscription.</span></span>

## <span data-ttu-id="aac3c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aac3c-107">EXAMPLES</span></span>

### <span data-ttu-id="aac3c-108">Przykład 1: uzyskiwanie informacji o rozmiarach ról</span><span class="sxs-lookup"><span data-stu-id="aac3c-108">Example 1: Get role size information</span></span>
```
PS C:\> Get-AzureRoleSize

          InstanceSize               : A6
          RoleSizeLabel              :
          Cores                      : 4
          MemoryInMb                 : 28672
          SupportedByWebWorkerRoles  : True
          SupportedByVirtualMachines : True
          OperationDescription       : Get-AzureRoleSize
          OperationId                : c5ed7b3a-03b3-548d-876b-6688c5b29cce
          OperationStatus            : Succeeded

          InstanceSize               : A7
          RoleSizeLabel              :
          Cores                      : 8
          MemoryInMb                 : 57344
          SupportedByWebWorkerRoles  : True
          SupportedByVirtualMachines : True
          OperationDescription       : Get-AzureRoleSize
          OperationId                : c5ed7b3a-03b3-548d-876b-6688c5b29cce
          OperationStatus            : Succeeded
```

<span data-ttu-id="aac3c-109">To polecenie uzyskuje informacje o rozmiarze roli dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="aac3c-109">This command gets role size information for the current subscription.</span></span>

### <span data-ttu-id="aac3c-110">Przykład 2: Uzyskaj informacje o rozmiarze roli i określ nazwę rozmiaru roli</span><span class="sxs-lookup"><span data-stu-id="aac3c-110">Example 2: Get role size information and specify the role size name</span></span>
```
PS C:\> Get-AzureRoleSize -InstanceSize A7

          InstanceSize               : A7
          RoleSizeLabel              :
          Cores                      : 8
          MemoryInMb                 : 57344
          SupportedByWebWorkerRoles  : True
          SupportedByVirtualMachines : True
          OperationDescription       : Get-AzureRoleSize
          OperationId                : c5ed7b3a-03b3-548d-876b-6688c5b29cce
          OperationStatus            : Succeeded
```

<span data-ttu-id="aac3c-111">To polecenie pobiera informacje o rozmiarze roli dla określonego rozmiaru roli.</span><span class="sxs-lookup"><span data-stu-id="aac3c-111">This command gets role size information for the specified role size.</span></span>

### <span data-ttu-id="aac3c-112">Przykład 3: uzyskiwanie informacji o rozmiarach ról dla wszystkich maszyn wirtualnych we wszystkich usługach platformy Azure</span><span class="sxs-lookup"><span data-stu-id="aac3c-112">Example 3: Get role size information for all virtual machines in all of the Azure services</span></span>
```
PS C:\> Get-AzureService | Get-AzureVM | Get-AzureRoleSize
```

<span data-ttu-id="aac3c-113">To polecenie pobiera informacje o rozmiarze roli dla wszystkich maszyn wirtualnych we wszystkich usługach platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="aac3c-113">This command gets role size information for all virtual machines in all of the Azure services.</span></span>

## <span data-ttu-id="aac3c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aac3c-114">PARAMETERS</span></span>

### <span data-ttu-id="aac3c-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="aac3c-115">-InformationAction</span></span>
<span data-ttu-id="aac3c-116">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="aac3c-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="aac3c-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="aac3c-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aac3c-118">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="aac3c-118">Continue</span></span>
- <span data-ttu-id="aac3c-119">Ignorować</span><span class="sxs-lookup"><span data-stu-id="aac3c-119">Ignore</span></span>
- <span data-ttu-id="aac3c-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="aac3c-120">Inquire</span></span>
- <span data-ttu-id="aac3c-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="aac3c-121">SilentlyContinue</span></span>
- <span data-ttu-id="aac3c-122">Przestaw</span><span class="sxs-lookup"><span data-stu-id="aac3c-122">Stop</span></span>
- <span data-ttu-id="aac3c-123">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="aac3c-123">Suspend</span></span>

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

### <span data-ttu-id="aac3c-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="aac3c-124">-InformationVariable</span></span>
<span data-ttu-id="aac3c-125">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="aac3c-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="aac3c-126">-InstanceSize</span><span class="sxs-lookup"><span data-stu-id="aac3c-126">-InstanceSize</span></span>
<span data-ttu-id="aac3c-127">Określa nazwę rozmiaru roli, na przykład: ExtraSmall, mały, duży, ExtraLarge, A5, A6.</span><span class="sxs-lookup"><span data-stu-id="aac3c-127">Specifies the role size name, for example: ExtraSmall, Small, Large, ExtraLarge, A5, A6, A7.</span></span>

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

### <span data-ttu-id="aac3c-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="aac3c-128">-Profile</span></span>
<span data-ttu-id="aac3c-129">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aac3c-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="aac3c-130">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="aac3c-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="aac3c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aac3c-131">CommonParameters</span></span>
<span data-ttu-id="aac3c-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aac3c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aac3c-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aac3c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aac3c-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aac3c-134">INPUTS</span></span>

## <span data-ttu-id="aac3c-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aac3c-135">OUTPUTS</span></span>

## <span data-ttu-id="aac3c-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aac3c-136">NOTES</span></span>

## <span data-ttu-id="aac3c-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aac3c-137">RELATED LINKS</span></span>

[<span data-ttu-id="aac3c-138">Get-AzureRole</span><span class="sxs-lookup"><span data-stu-id="aac3c-138">Get-AzureRole</span></span>](./Get-AzureRole.md)

[<span data-ttu-id="aac3c-139">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="aac3c-139">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="aac3c-140">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="aac3c-140">Get-AzureVM</span></span>](./Get-AzureVM.md)


