---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9999E0EE-4A32-4C18-A6EC-2A073DC08710
online version: ''
schema: 2.0.0
ms.openlocfilehash: e5dfe0f42987ba51613ff9bafa000713456dfaf7
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "94061881"
---
# <span data-ttu-id="7da4d-101">Remove-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="7da4d-101">Remove-WAPackVMRole</span></span>

## <span data-ttu-id="7da4d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7da4d-102">SYNOPSIS</span></span>
<span data-ttu-id="7da4d-103">Usuwa obiekty roli maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7da4d-103">Removes virtual machine role objects.</span></span>

## <span data-ttu-id="7da4d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7da4d-104">SYNTAX</span></span>

### <span data-ttu-id="7da4d-105">FromVMRoleObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7da4d-105">FromVMRoleObject (Default)</span></span>
```
Remove-WAPackVMRole -VMRole <VMRole> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7da4d-106">FromCloudService</span><span class="sxs-lookup"><span data-stu-id="7da4d-106">FromCloudService</span></span>
```
Remove-WAPackVMRole -VMRole <VMRole> -CloudServiceName <String> [-PassThru] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7da4d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7da4d-107">DESCRIPTION</span></span>
<span data-ttu-id="7da4d-108">Te tematy są przestarzałe i zostaną usunięte w przyszłości.</span><span class="sxs-lookup"><span data-stu-id="7da4d-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="7da4d-109">W tym temacie opisano polecenie cmdlet w wersji 0.8.1 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7da4d-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7da4d-110">Aby sprawdzić używaną wersję modułu, należy wpisać ją w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="7da4d-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7da4d-111">Polecenie cmdlet **Remove-WAPackVMRole** usuwa obiekty roli maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7da4d-111">The **Remove-WAPackVMRole** cmdlet removes virtual machine role objects.</span></span>

## <span data-ttu-id="7da4d-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7da4d-112">EXAMPLES</span></span>

### <span data-ttu-id="7da4d-113">Przykład 1: Usuwanie roli maszyny wirtualnej (utworzonej za pomocą portalu WAP)</span><span class="sxs-lookup"><span data-stu-id="7da4d-113">Example 1: Remove a virtual machine role (which was created using the WAP portal)</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole01"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole
```

<span data-ttu-id="7da4d-114">Pierwsze polecenie uzyskuje rolę maszyny wirtualnej o nazwie ContosoVMRole01 przy użyciu polecenia cmdlet **Get-WAPackVMRole** , a następnie zapisuje ten obiekt w zmiennej $VMRole.</span><span class="sxs-lookup"><span data-stu-id="7da4d-114">The first command gets the virtual machine role named ContosoVMRole01 by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="7da4d-115">Drugie polecenie usuwa rolę maszyny wirtualnej przechowywaną w $VMRole.</span><span class="sxs-lookup"><span data-stu-id="7da4d-115">The second command removes the virtual machine role stored in $VMRole.</span></span>
<span data-ttu-id="7da4d-116">Polecenie wyświetli monit o potwierdzenie. Zakładając, że ta rola maszyny wirtualnej została utworzona za pomocą portalu WAP, nie trzeba określać nazwy usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="7da4d-116">The command prompts you for confirmation.Assuming this virtual machine role was created using the WAP portal, there's no need to specify the cloud service name.</span></span>

### <span data-ttu-id="7da4d-117">Przykład 2: Usuwanie roli maszyny wirtualnej utworzonej po ręcznym utworzeniu usługi w chmurze</span><span class="sxs-lookup"><span data-stu-id="7da4d-117">Example 2: Remove a virtual machine role which was created after manually creating a cloud service</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole02"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -CloudServiceName "ContosoCloudService02"
```

<span data-ttu-id="7da4d-118">Pierwsze polecenie uzyskuje rolę maszyny wirtualnej o nazwie "ContosoVMRole02" przy użyciu polecenia cmdlet **Get-WAPackVMRole** , a następnie zapisuje ten obiekt w zmiennej $VMRole.</span><span class="sxs-lookup"><span data-stu-id="7da4d-118">The first command gets the virtual machine role named "ContosoVMRole02" by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="7da4d-119">Drugie polecenie usuwa rolę maszyny wirtualnej przechowywaną w $VMRole.</span><span class="sxs-lookup"><span data-stu-id="7da4d-119">The second command removes the virtual machine role stored in $VMRole.</span></span>
<span data-ttu-id="7da4d-120">Polecenie wyświetli monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7da4d-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="7da4d-121">Zakładając, że ta rola maszyny wirtualnej nie została utworzona za pomocą portalu, użytkownik musi określić nazwę usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="7da4d-121">Assuming this virtual machine role was not created using the portal, the user needs to specify the cloud service name.</span></span>
<span data-ttu-id="7da4d-122">W tym przypadku o nazwie "ContosoCloudService02".</span><span class="sxs-lookup"><span data-stu-id="7da4d-122">In this case named "ContosoCloudService02".</span></span>

### <span data-ttu-id="7da4d-123">Przykład 3: Usuwanie roli maszyny wirtualnej bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="7da4d-123">Example 3: Remove a virtual machine role without confirmation</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole03"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -Force
```

<span data-ttu-id="7da4d-124">Pierwsze polecenie uzyskuje usługę w chmurze o nazwie ContosoVMRole03 przy użyciu polecenia cmdlet **Get-WAPackVMRole** , a następnie zapisuje ten obiekt w zmiennej $VMRole.</span><span class="sxs-lookup"><span data-stu-id="7da4d-124">The first command gets the cloud service named ContosoVMRole03 by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="7da4d-125">Drugie polecenie usuwa rolę maszyny wirtualnej przechowywaną w $VMRole.</span><span class="sxs-lookup"><span data-stu-id="7da4d-125">The second command removes the virtual machine role stored in $VMRole.</span></span>
<span data-ttu-id="7da4d-126">To polecenie zawiera parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="7da4d-126">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="7da4d-127">Polecenie nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7da4d-127">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="7da4d-128">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7da4d-128">PARAMETERS</span></span>

### <span data-ttu-id="7da4d-129">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="7da4d-129">-CloudServiceName</span></span>
<span data-ttu-id="7da4d-130">Określa nazwę usługi w chmurze dla roli maszyna wirtualna.</span><span class="sxs-lookup"><span data-stu-id="7da4d-130">Specifies the cloud service name of virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7da4d-131">-Force</span><span class="sxs-lookup"><span data-stu-id="7da4d-131">-Force</span></span>
<span data-ttu-id="7da4d-132">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7da4d-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7da4d-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7da4d-133">-PassThru</span></span>
<span data-ttu-id="7da4d-134">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="7da4d-134">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7da4d-135">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="7da4d-135">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7da4d-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="7da4d-136">-Profile</span></span>
<span data-ttu-id="7da4d-137">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7da4d-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7da4d-138">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="7da4d-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7da4d-139">-VMRole</span><span class="sxs-lookup"><span data-stu-id="7da4d-139">-VMRole</span></span>
<span data-ttu-id="7da4d-140">Określa rolę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7da4d-140">Specifies a virtual machine role.</span></span>
<span data-ttu-id="7da4d-141">Aby uzyskać rolę maszyny wirtualnej, użyj polecenia cmdlet **Get-WAPackVMRole** .</span><span class="sxs-lookup"><span data-stu-id="7da4d-141">To get a virtual machine role, use the **Get-WAPackVMRole** cmdlet.</span></span>

```yaml
Type: VMRole
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7da4d-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7da4d-142">-Confirm</span></span>
<span data-ttu-id="7da4d-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7da4d-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7da4d-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7da4d-144">-WhatIf</span></span>
<span data-ttu-id="7da4d-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7da4d-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7da4d-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7da4d-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7da4d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7da4d-147">CommonParameters</span></span>
<span data-ttu-id="7da4d-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7da4d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7da4d-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7da4d-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7da4d-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7da4d-150">INPUTS</span></span>

## <span data-ttu-id="7da4d-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7da4d-151">OUTPUTS</span></span>

## <span data-ttu-id="7da4d-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7da4d-152">NOTES</span></span>

## <span data-ttu-id="7da4d-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7da4d-153">RELATED LINKS</span></span>

[<span data-ttu-id="7da4d-154">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="7da4d-154">Get-WAPackVMRole</span></span>](./Get-WAPackVMRole.md)

[<span data-ttu-id="7da4d-155">Nowe — WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="7da4d-155">New-WAPackVMRole</span></span>](./New-WAPackVMRole.md)

[<span data-ttu-id="7da4d-156">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="7da4d-156">Set-WAPackVMRole</span></span>](./Set-WAPackVMRole.md)


