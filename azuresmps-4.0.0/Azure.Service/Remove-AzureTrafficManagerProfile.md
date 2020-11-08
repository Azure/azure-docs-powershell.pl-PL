---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: B96A64DD-9005-4B04-A720-6FCF33797E8D
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1fa73aa4e38c8d222da6e73508e9a18a15c1e3f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055057"
---
# <span data-ttu-id="d88f6-101">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d88f6-101">Remove-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="d88f6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d88f6-102">SYNOPSIS</span></span>
<span data-ttu-id="d88f6-103">Usuwa profil w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="d88f6-103">Removes a Traffic Manager profile.</span></span>

## <span data-ttu-id="d88f6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d88f6-104">SYNTAX</span></span>

```
Remove-AzureTrafficManagerProfile -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d88f6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d88f6-105">DESCRIPTION</span></span>
<span data-ttu-id="d88f6-106">Polecenie cmdlet **Remove-AzureTrafficManagerProfile** usuwa profil usługi Microsoft Azure Traffic Manager z bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d88f6-106">The **Remove-AzureTrafficManagerProfile** cmdlet removes a Microsoft Azure Traffic Manager profile from the current subscription.</span></span>

## <span data-ttu-id="d88f6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d88f6-107">EXAMPLES</span></span>

### <span data-ttu-id="d88f6-108">Przykład 1: Usuwanie profilu w usłudze Traffic Manager</span><span class="sxs-lookup"><span data-stu-id="d88f6-108">Example 1: Remove a Traffic Manager profile</span></span>
```
PS C:\>Remove-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="d88f6-109">To polecenie usuwa profil usługi Traffic Manager o nazwie Moja profil.</span><span class="sxs-lookup"><span data-stu-id="d88f6-109">This command removes the Traffic Manager profile named MyProfile.</span></span>

### <span data-ttu-id="d88f6-110">Przykład 2: Usuwanie profilu w usłudze Traffic Manager</span><span class="sxs-lookup"><span data-stu-id="d88f6-110">Example 2: Remove a Traffic Manager profile</span></span>
```
PS C:\>Remove-AzureTrafficManagerProfile -Name "MyProfile" -Force -PassThru
```

<span data-ttu-id="d88f6-111">To polecenie usuwa profil usługi Traffic Manager o nazwie Moja profil bez monitowania o potwierdzenie i zwraca wyniki.</span><span class="sxs-lookup"><span data-stu-id="d88f6-111">This command removes the Traffic Manager profile named MyProfile without prompting you for confirmation, and returns the results.</span></span>

## <span data-ttu-id="d88f6-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d88f6-112">PARAMETERS</span></span>

### <span data-ttu-id="d88f6-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d88f6-113">-Force</span></span>
<span data-ttu-id="d88f6-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d88f6-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d88f6-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d88f6-115">-Name</span></span>
<span data-ttu-id="d88f6-116">Określa nazwę profilu usługi Traffic Manager, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="d88f6-116">Specifies the name of the Traffic Manager profile to delete.</span></span>

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

### <span data-ttu-id="d88f6-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d88f6-117">-PassThru</span></span>
<span data-ttu-id="d88f6-118">Zwraca $True, jeśli operacja zakończyła się pomyślnie; w przeciwnym razie $False.</span><span class="sxs-lookup"><span data-stu-id="d88f6-118">Returns $True if the operation succeeded; otherwise, $False.</span></span>
<span data-ttu-id="d88f6-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="d88f6-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d88f6-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="d88f6-120">-Profile</span></span>
<span data-ttu-id="d88f6-121">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d88f6-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d88f6-122">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="d88f6-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d88f6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d88f6-123">CommonParameters</span></span>
<span data-ttu-id="d88f6-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d88f6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d88f6-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d88f6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d88f6-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d88f6-126">INPUTS</span></span>

## <span data-ttu-id="d88f6-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d88f6-127">OUTPUTS</span></span>

### <span data-ttu-id="d88f6-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d88f6-128">System.Boolean</span></span>
<span data-ttu-id="d88f6-129">To polecenie cmdlet generuje $True lub $False.</span><span class="sxs-lookup"><span data-stu-id="d88f6-129">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="d88f6-130">Jeśli operacja kończy się powodzeniem, a jeśli określisz parametr *PassThru* , to polecenie cmdlet zwróci wartość $true.</span><span class="sxs-lookup"><span data-stu-id="d88f6-130">If the operation is successful and if you specify the *PassThru* parameter, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="d88f6-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d88f6-131">NOTES</span></span>

## <span data-ttu-id="d88f6-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d88f6-132">RELATED LINKS</span></span>

[<span data-ttu-id="d88f6-133">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d88f6-133">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="d88f6-134">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d88f6-134">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="d88f6-135">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d88f6-135">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="d88f6-136">Nowe — AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d88f6-136">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="d88f6-137">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d88f6-137">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


