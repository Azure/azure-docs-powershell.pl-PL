---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: ABC303ED-8712-4958-B871-E95357012277
online version: ''
schema: 2.0.0
ms.openlocfilehash: 706c1dee2bc4bb21a8cf116d15bfa3e53daeed99
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055061"
---
# <span data-ttu-id="44756-101">Remove-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="44756-101">Remove-AzureSubscription</span></span>

## <span data-ttu-id="44756-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="44756-102">SYNOPSIS</span></span>
<span data-ttu-id="44756-103">Usuwa subskrypcję platformy Azure z programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="44756-103">Deletes an Azure subscription from Windows PowerShell.</span></span>

## <span data-ttu-id="44756-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="44756-104">SYNTAX</span></span>

### <span data-ttu-id="44756-105">Nazwa (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="44756-105">Name (Default)</span></span>
```
Remove-AzureSubscription -SubscriptionName <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44756-106">Identyfikacji</span><span class="sxs-lookup"><span data-stu-id="44756-106">Id</span></span>
```
Remove-AzureSubscription -SubscriptionId <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44756-107">Opis</span><span class="sxs-lookup"><span data-stu-id="44756-107">DESCRIPTION</span></span>
<span data-ttu-id="44756-108">Polecenie cmdlet **Remove-AzureSubscription** usuwa subskrypcję platformy Azure z pliku danych abonamentu, aby program Windows PowerShell mógł go znaleźć.</span><span class="sxs-lookup"><span data-stu-id="44756-108">The **Remove-AzureSubscription** cmdlet deletes an Azure subscription from your subscription data file so Windows PowerShell can't find it.</span></span>
<span data-ttu-id="44756-109">To polecenie cmdlet nie powoduje usunięcia subskrypcji z usługi Microsoft Azure ani w jakikolwiek sposób zmieniania abonamentu rzeczywistego.</span><span class="sxs-lookup"><span data-stu-id="44756-109">This cmdlet does not delete the subscription from Microsoft Azure, or change the actual subscription in any way.</span></span>

<span data-ttu-id="44756-110">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="44756-110">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="44756-111">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="44756-111">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="44756-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="44756-112">EXAMPLES</span></span>

### <span data-ttu-id="44756-113">Przykład 1: usuwanie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="44756-113">Example 1: Delete a subscription</span></span>
```
C:\PS> Remove-AzureSubscription -SubscriptionName Test

Confirm
Are you sure you want to perform this action?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="44756-114">To polecenie usuwa abonament "test" z domyślnego pliku danych subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="44756-114">This command deletes the "Test" subscription from the default subscription data file.</span></span>

### <span data-ttu-id="44756-115">Przykład 2: usuwanie z alternatywnego pliku danych subskrypcji</span><span class="sxs-lookup"><span data-stu-id="44756-115">Example 2: Delete from an alternate subscription data file</span></span>
```
C:\PS> Remove-AzureSubscription -SubscriptionName Test -SubscriptionDataFile C:\Subs\MySubscriptions.xml -Force
```

<span data-ttu-id="44756-116">To polecenie powoduje usunięcie subskrypcji testowej z pliku danych abonamentu MySubscriptions.xml.</span><span class="sxs-lookup"><span data-stu-id="44756-116">This command deletes the Test subscription from the MySubscriptions.xml subscription data file.</span></span>
<span data-ttu-id="44756-117">W poleceniu użyto parametru *Force* w celu wyminięcia monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="44756-117">The command uses the *Force* parameter to suppress the confirmation prompt.</span></span>

### <span data-ttu-id="44756-118">Przykład 3: usuwanie subskrypcji ze skryptu</span><span class="sxs-lookup"><span data-stu-id="44756-118">Example 3: Delete a subscription in a script</span></span>
```
C:\PS> ...if (Remove-AzureSubscription -SubscriptionName Test -PassThru) {...}
```

<span data-ttu-id="44756-119">To polecenie używa polecenia **Remove-AzureSubscription** w instrukcji **Jeżeli** .</span><span class="sxs-lookup"><span data-stu-id="44756-119">This command uses the **Remove-AzureSubscription** command in an **If** statement.</span></span>
<span data-ttu-id="44756-120">Używa parametru *PassThru* , który zwraca wartość logiczną, aby określić, czy blok skryptu w instrukcji **Jeżeli** jest wykonywany.</span><span class="sxs-lookup"><span data-stu-id="44756-120">It uses the *PassThru* parameter, which returns a Boolean value, to determine whether the script block in the **If** statement is executed.</span></span>

## <span data-ttu-id="44756-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="44756-121">PARAMETERS</span></span>

### <span data-ttu-id="44756-122">-Force</span><span class="sxs-lookup"><span data-stu-id="44756-122">-Force</span></span>
<span data-ttu-id="44756-123">Pomija monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="44756-123">Suppresses the confirmation prompt.</span></span>

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

### <span data-ttu-id="44756-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44756-124">-PassThru</span></span>
<span data-ttu-id="44756-125">Zwraca wartość $True, jeśli wykonanie polecenia powiedzie się i $False, jeśli nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="44756-125">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="44756-126">Domyślnie to polecenie cmdlet nie zwraca żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="44756-126">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="44756-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="44756-127">-Profile</span></span>
<span data-ttu-id="44756-128">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44756-128">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="44756-129">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="44756-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="44756-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="44756-130">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: Id
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44756-131">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="44756-131">-SubscriptionName</span></span>
```yaml
Type: String
Parameter Sets: Name
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44756-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="44756-132">-Confirm</span></span>
<span data-ttu-id="44756-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44756-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44756-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44756-134">-WhatIf</span></span>
<span data-ttu-id="44756-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44756-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44756-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="44756-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44756-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44756-137">CommonParameters</span></span>
<span data-ttu-id="44756-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44756-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44756-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44756-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44756-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44756-140">INPUTS</span></span>

### <span data-ttu-id="44756-141">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="44756-141">None</span></span>
<span data-ttu-id="44756-142">Możesz popotokować dane wejściowe tego polecenia cmdlet, korzystając z nazwy właściwości, ale nie według wartości.</span><span class="sxs-lookup"><span data-stu-id="44756-142">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="44756-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="44756-143">OUTPUTS</span></span>

### <span data-ttu-id="44756-144">Brak lub system. Boolean</span><span class="sxs-lookup"><span data-stu-id="44756-144">None or System.Boolean</span></span>
<span data-ttu-id="44756-145">W przypadku użycia parametru *PassThru* to polecenie cmdlet zwraca wartość logiczną.</span><span class="sxs-lookup"><span data-stu-id="44756-145">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="44756-146">W przeciwnym razie nie zwróci żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="44756-146">Otherwise, it does not return any output.</span></span>

## <span data-ttu-id="44756-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="44756-147">NOTES</span></span>

## <span data-ttu-id="44756-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="44756-148">RELATED LINKS</span></span>

[<span data-ttu-id="44756-149">Get-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="44756-149">Get-AzureSubscription</span></span>](./Get-AzureSubscription.md)

[<span data-ttu-id="44756-150">Wybierz — AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="44756-150">Select-AzureSubscription</span></span>](./Select-AzureSubscription.md)

[<span data-ttu-id="44756-151">Set-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="44756-151">Set-AzureSubscription</span></span>](./Set-AzureSubscription.md)


