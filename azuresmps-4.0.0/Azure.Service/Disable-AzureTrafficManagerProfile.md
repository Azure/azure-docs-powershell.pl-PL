---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: ECE9C2A6-7DA2-4477-B877-9970FBE26D7C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8f378cbf8926a650699ec50a2a0a42873dcb7528
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054659"
---
# <span data-ttu-id="36886-101">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="36886-101">Disable-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="36886-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="36886-102">SYNOPSIS</span></span>
<span data-ttu-id="36886-103">Wyłącza profil w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="36886-103">Disables a Traffic Manager profile.</span></span>

## <span data-ttu-id="36886-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="36886-104">SYNTAX</span></span>

```
Disable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="36886-105">Opis</span><span class="sxs-lookup"><span data-stu-id="36886-105">DESCRIPTION</span></span>
<span data-ttu-id="36886-106">Polecenie cmdlet **disable-AzureTrafficManagerProfile** wyłącza profil usługi Microsoft Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="36886-106">The **Disable-AzureTrafficManagerProfile** cmdlet disables a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="36886-107">Za pomocą parametru *PassThru* można wyświetlać, czy operacja kończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="36886-107">You can use the *PassThru* parameter to display whether the operation succeeds.</span></span>

## <span data-ttu-id="36886-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="36886-108">EXAMPLES</span></span>

### <span data-ttu-id="36886-109">Przykład 1: wyłączenie profilu usługi Traffic Manager i wyświetlenie wyników</span><span class="sxs-lookup"><span data-stu-id="36886-109">Example 1: Disable a Traffic Manager profile and display the results</span></span>
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

<span data-ttu-id="36886-110">To polecenie wyłącza profil usługi Traffic Manager o nazwie Moja profil.</span><span class="sxs-lookup"><span data-stu-id="36886-110">This command disables the Traffic Manager profile named MyProfile.</span></span>
<span data-ttu-id="36886-111">To polecenie określa parametr *PassThru* , który ma być wyświetlany, gdy polecenie zostało pomyślnie zakończone.</span><span class="sxs-lookup"><span data-stu-id="36886-111">The command specifies the *PassThru* parameter to display whether the command succeeded.</span></span>

### <span data-ttu-id="36886-112">Przykład 2: wyłączenie profilu w usłudze Traffic Manager i wyświetlenie brakujących wyników</span><span class="sxs-lookup"><span data-stu-id="36886-112">Example 2: Disable a Traffic Manager profile and display no results</span></span>
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="36886-113">To polecenie wyłącza profil usługi Traffic Manager o nazwie Moja profil, ale nie wyświetla tego, czy polecenie zostało pomyślnie zakończone.</span><span class="sxs-lookup"><span data-stu-id="36886-113">This command disables the Traffic Manager profile named MyProfile but does not display whether the command succeeded.</span></span>

## <span data-ttu-id="36886-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="36886-114">PARAMETERS</span></span>

### <span data-ttu-id="36886-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="36886-115">-Name</span></span>
<span data-ttu-id="36886-116">Określa nazwę profilu usługi Traffic Manager, który ma zostać wyłączony.</span><span class="sxs-lookup"><span data-stu-id="36886-116">Specifies the name of the Traffic Manager profile to disable.</span></span>

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

### <span data-ttu-id="36886-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36886-117">-PassThru</span></span>
<span data-ttu-id="36886-118">Zwraca $True, jeśli operacja zakończyła się pomyślnie; w przeciwnym razie $False.</span><span class="sxs-lookup"><span data-stu-id="36886-118">Returns $True if the operation succeeded; otherwise, $False.</span></span>
<span data-ttu-id="36886-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="36886-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="36886-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="36886-120">-Profile</span></span>
<span data-ttu-id="36886-121">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36886-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="36886-122">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="36886-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="36886-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36886-123">CommonParameters</span></span>
<span data-ttu-id="36886-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36886-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36886-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36886-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36886-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36886-126">INPUTS</span></span>

## <span data-ttu-id="36886-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="36886-127">OUTPUTS</span></span>

### <span data-ttu-id="36886-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="36886-128">System.Boolean</span></span>
<span data-ttu-id="36886-129">To polecenie cmdlet generuje $True lub $False.</span><span class="sxs-lookup"><span data-stu-id="36886-129">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="36886-130">Jeśli operacja kończy się powodzeniem, a jeśli określisz parametr *PassThru* , to polecenie cmdlet zwróci wartość $true.</span><span class="sxs-lookup"><span data-stu-id="36886-130">If the operation is successful and if you specify the *PassThru* parameter, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="36886-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="36886-131">NOTES</span></span>

## <span data-ttu-id="36886-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36886-132">RELATED LINKS</span></span>

[<span data-ttu-id="36886-133">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="36886-133">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="36886-134">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="36886-134">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="36886-135">Nowe — AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="36886-135">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="36886-136">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="36886-136">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="36886-137">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="36886-137">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


