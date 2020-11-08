---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 5D093C10-F8B6-4F4A-ABD7-CC4D7AB7AFFA
online version: ''
schema: 2.0.0
ms.openlocfilehash: c78f53b95d18de600535368a1109b318294928c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054918"
---
# <span data-ttu-id="5975e-101">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="5975e-101">Set-AzureServiceProjectRole</span></span>

## <span data-ttu-id="5975e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5975e-102">SYNOPSIS</span></span>
<span data-ttu-id="5975e-103">Ustawia liczbę wystąpień lub wersję wykonawczą roli.</span><span class="sxs-lookup"><span data-stu-id="5975e-103">Sets the number of instances or the runtime version of a role.</span></span>

## <span data-ttu-id="5975e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5975e-104">SYNTAX</span></span>

### <span data-ttu-id="5975e-105">Instance</span><span class="sxs-lookup"><span data-stu-id="5975e-105">Instances</span></span>
```
Set-AzureServiceProjectRole [-RoleName <String>] -Instances <Int32> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="5975e-106">Runtime</span><span class="sxs-lookup"><span data-stu-id="5975e-106">Runtime</span></span>
```
Set-AzureServiceProjectRole [-RoleName <String>] -Runtime <String> -Version <String> [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5975e-107">VMSize</span><span class="sxs-lookup"><span data-stu-id="5975e-107">VMSize</span></span>
```
Set-AzureServiceProjectRole [-RoleName <String>] [-PassThru] -VMSize <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="5975e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5975e-108">DESCRIPTION</span></span>
<span data-ttu-id="5975e-109">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5975e-109">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="5975e-110">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="5975e-110">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="5975e-111">Polecenie cmdlet **Set-AzureServiceProjectRole** ustawia liczbę wystąpień roli dla określonej roli.</span><span class="sxs-lookup"><span data-stu-id="5975e-111">The **Set-AzureServiceProjectRole** cmdlet sets the number of role instances for the specified role.</span></span>

## <span data-ttu-id="5975e-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5975e-112">EXAMPLES</span></span>

### <span data-ttu-id="5975e-113">Przykład 1: Ustawianie wystąpień roli sieci Web</span><span class="sxs-lookup"><span data-stu-id="5975e-113">Example 1: Set instances for a web role</span></span>
```
PS C:\> Set-AzureServiceProjectRole "MyWebRole" 2
```

<span data-ttu-id="5975e-114">Ustawia liczbę wystąpień roli sieci Web o nazwie MyWebRole1 na wartość 2.</span><span class="sxs-lookup"><span data-stu-id="5975e-114">Sets the number of instances for the web role named MyWebRole1 to 2.</span></span>

### <span data-ttu-id="5975e-115">Przykład 2: Ustawianie wystąpień roli pracownika</span><span class="sxs-lookup"><span data-stu-id="5975e-115">Example 2: Set instances for a worker role</span></span>
```
PS C:\> Set-AzureServiceProjectRole "MyWorkerRole1" 2
```

<span data-ttu-id="5975e-116">Ustawia liczbę wystąpień roli dla roli pracownika o nazwie WorkerRole1 na 2.</span><span class="sxs-lookup"><span data-stu-id="5975e-116">Sets the role instance count for the worker role named WorkerRole1 to 2.</span></span>

### <span data-ttu-id="5975e-117">Przykład 3: Ustawianie wersji środowiska wykonawczego dla usługi roli</span><span class="sxs-lookup"><span data-stu-id="5975e-117">Example 3: Set the runtime version for a role service</span></span>
```
PS C:\> Set-AzureServiceProjectRole "MyRole1" node 0.6.20
```

<span data-ttu-id="5975e-118">Ustawia node.exeą wersję środowiska wykonawczego dla roli MyRole1 na 0.6.20.</span><span class="sxs-lookup"><span data-stu-id="5975e-118">Sets the node.exe runtime version for role MyRole1 to 0.6.20.</span></span>

## <span data-ttu-id="5975e-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5975e-119">PARAMETERS</span></span>

### <span data-ttu-id="5975e-120">-Wystąpienia</span><span class="sxs-lookup"><span data-stu-id="5975e-120">-Instances</span></span>
<span data-ttu-id="5975e-121">Określa liczbę wystąpień roli dla określonej roli w sieci Web lub w ramach procesu roboczego.</span><span class="sxs-lookup"><span data-stu-id="5975e-121">Specifies the number of role instances for the specified web or worker role.</span></span>

```yaml
Type: Int32
Parameter Sets: Instances
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5975e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5975e-122">-PassThru</span></span>
<span data-ttu-id="5975e-123">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="5975e-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5975e-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="5975e-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5975e-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="5975e-125">-Profile</span></span>
<span data-ttu-id="5975e-126">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5975e-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5975e-127">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="5975e-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5975e-128">-Rolename</span><span class="sxs-lookup"><span data-stu-id="5975e-128">-RoleName</span></span>
<span data-ttu-id="5975e-129">Określa nazwę roli sieci Web lub procesu roboczego, która ma zostać zmieniona.</span><span class="sxs-lookup"><span data-stu-id="5975e-129">Specifies the name of the web or worker role to be changed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5975e-130">-Runtime</span><span class="sxs-lookup"><span data-stu-id="5975e-130">-Runtime</span></span>
<span data-ttu-id="5975e-131">Określa środowisko uruchomieniowe, które ma zostać dodane do określonej roli.</span><span class="sxs-lookup"><span data-stu-id="5975e-131">Specifies the runtime to add to the specified role.</span></span>

```yaml
Type: String
Parameter Sets: Runtime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5975e-132">-Version</span><span class="sxs-lookup"><span data-stu-id="5975e-132">-Version</span></span>
<span data-ttu-id="5975e-133">Określa wersję środowiska uruchomieniowego, którą należy dodać do roli.</span><span class="sxs-lookup"><span data-stu-id="5975e-133">Specifies the version of the runtime to add to the role.</span></span>

```yaml
Type: String
Parameter Sets: Runtime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5975e-134">-VMSize</span><span class="sxs-lookup"><span data-stu-id="5975e-134">-VMSize</span></span>
<span data-ttu-id="5975e-135">Określa rozmiar maszyny wirtualnej roli.</span><span class="sxs-lookup"><span data-stu-id="5975e-135">Specifies the virtual machine size of the role.</span></span>

```yaml
Type: String
Parameter Sets: VMSize
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5975e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5975e-136">CommonParameters</span></span>
<span data-ttu-id="5975e-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5975e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5975e-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5975e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5975e-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5975e-139">INPUTS</span></span>

###  
<span data-ttu-id="5975e-140">Określa rozmiar maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5975e-140">Specifies the size of the virtual machine.</span></span>

## <span data-ttu-id="5975e-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5975e-141">OUTPUTS</span></span>

## <span data-ttu-id="5975e-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5975e-142">NOTES</span></span>

## <span data-ttu-id="5975e-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5975e-143">RELATED LINKS</span></span>

[<span data-ttu-id="5975e-144">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="5975e-144">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)


