---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1ECF6BB5-3751-4DA0-AC6C-A64F15F46D26
online version: ''
schema: 2.0.0
ms.openlocfilehash: 552c2511a806abb4329860e7c15d8a68b5e03f79
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "94061883"
---
# <span data-ttu-id="3fd3c-101">Remove-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="3fd3c-101">Remove-WAPackCloudService</span></span>

## <span data-ttu-id="3fd3c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3fd3c-102">SYNOPSIS</span></span>
<span data-ttu-id="3fd3c-103">Usuwa obiekty usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="3fd3c-103">Removes cloud service objects.</span></span>

## <span data-ttu-id="3fd3c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3fd3c-104">SYNTAX</span></span>

```
Remove-WAPackCloudService -CloudService <CloudService> [-PassThru] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fd3c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3fd3c-105">DESCRIPTION</span></span>
<span data-ttu-id="3fd3c-106">Te tematy są przestarzałe i zostaną usunięte w przyszłości.</span><span class="sxs-lookup"><span data-stu-id="3fd3c-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="3fd3c-107">W tym temacie opisano polecenie cmdlet w wersji 0.8.1 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3fd3c-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="3fd3c-108">Aby sprawdzić używaną wersję modułu, należy wpisać ją w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="3fd3c-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="3fd3c-109">Polecenie cmdlet **Remove-WAPackCloudService** usuwa obiekty usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="3fd3c-109">The **Remove-WAPackCloudService** cmdlet removes cloud service objects.</span></span>

## <span data-ttu-id="3fd3c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3fd3c-110">EXAMPLES</span></span>

### <span data-ttu-id="3fd3c-111">Przykład 1: Usuwanie usługi w chmurze</span><span class="sxs-lookup"><span data-stu-id="3fd3c-111">Example 1: Remove a cloud service</span></span>
```
PS C:\> $CloudService = Get-WAPackCloudService -Name "ContosoCloudService01"
PS C:\> Remove-WAPackVM -VM $CloudService
```

<span data-ttu-id="3fd3c-112">Pierwsze polecenie uzyskuje usługę w chmurze o nazwie ContosoCloudService01 przy użyciu polecenia cmdlet **Get-WAPackCloudService** , a następnie zapisuje ten obiekt w zmiennej $CloudService.</span><span class="sxs-lookup"><span data-stu-id="3fd3c-112">The first command gets the cloud service named ContosoCloudService01 by using the **Get-WAPackCloudService** cmdlet, and then stores that object in the $CloudService variable.</span></span>

<span data-ttu-id="3fd3c-113">Drugie polecenie usuwa CloudService zapisane w $CloudService.</span><span class="sxs-lookup"><span data-stu-id="3fd3c-113">The second command removes the cloudservice stored in $CloudService.</span></span>
<span data-ttu-id="3fd3c-114">Polecenie wyświetli monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3fd3c-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="3fd3c-115">Przykład 2: Usunięcie usługi w chmurze bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="3fd3c-115">Example 2: Remove a cloud service without confirmation</span></span>
```
PS C:\> $CloudService = Get-WAPackCloudService -Name "ContosoCloudService02"
PS C:\> Remove-WAPackCloudService -VM $CloudService -Force
```

<span data-ttu-id="3fd3c-116">Pierwsze polecenie uzyskuje usługę w chmurze o nazwie ContosoCloudService02 przy użyciu polecenia cmdlet **Get-WAPackCloudService** , a następnie zapisuje ten obiekt w zmiennej $CloudService.</span><span class="sxs-lookup"><span data-stu-id="3fd3c-116">The first command gets the cloud service named ContosoCloudService02 by using the **Get-WAPackCloudService** cmdlet, and then stores that object in the $CloudService variable.</span></span>

<span data-ttu-id="3fd3c-117">Drugie polecenie usuwa usługę w chmurze przechowywaną w $CloudService.</span><span class="sxs-lookup"><span data-stu-id="3fd3c-117">The second command removes the cloud service stored in $CloudService.</span></span>
<span data-ttu-id="3fd3c-118">To polecenie zawiera parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="3fd3c-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="3fd3c-119">Polecenie nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3fd3c-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="3fd3c-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3fd3c-120">PARAMETERS</span></span>

### <span data-ttu-id="3fd3c-121">-CloudService</span><span class="sxs-lookup"><span data-stu-id="3fd3c-121">-CloudService</span></span>
<span data-ttu-id="3fd3c-122">Określa obiekt usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="3fd3c-122">Specifies a cloud service object.</span></span>
<span data-ttu-id="3fd3c-123">Aby uzyskać usługę w chmurze, użyj polecenia cmdlet **Get-WAPackCloudService** .</span><span class="sxs-lookup"><span data-stu-id="3fd3c-123">To obtain a cloud service, use the **Get-WAPackCloudService** cmdlet.</span></span>

```yaml
Type: CloudService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3fd3c-124">-Force</span><span class="sxs-lookup"><span data-stu-id="3fd3c-124">-Force</span></span>
<span data-ttu-id="3fd3c-125">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3fd3c-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3fd3c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3fd3c-126">-PassThru</span></span>
<span data-ttu-id="3fd3c-127">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="3fd3c-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3fd3c-128">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="3fd3c-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3fd3c-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="3fd3c-129">-Profile</span></span>
<span data-ttu-id="3fd3c-130">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fd3c-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3fd3c-131">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="3fd3c-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3fd3c-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3fd3c-132">-Confirm</span></span>
<span data-ttu-id="3fd3c-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fd3c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fd3c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fd3c-134">-WhatIf</span></span>
<span data-ttu-id="3fd3c-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fd3c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fd3c-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3fd3c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fd3c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fd3c-137">CommonParameters</span></span>
<span data-ttu-id="3fd3c-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fd3c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fd3c-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fd3c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fd3c-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3fd3c-140">INPUTS</span></span>

## <span data-ttu-id="3fd3c-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3fd3c-141">OUTPUTS</span></span>

## <span data-ttu-id="3fd3c-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3fd3c-142">NOTES</span></span>

## <span data-ttu-id="3fd3c-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3fd3c-143">RELATED LINKS</span></span>

[<span data-ttu-id="3fd3c-144">Get-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="3fd3c-144">Get-WAPackCloudService</span></span>](./Get-WAPackCloudService.md)

[<span data-ttu-id="3fd3c-145">Nowe — WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="3fd3c-145">New-WAPackCloudService</span></span>](./New-WAPackCloudService.md)


