---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 6ACE045E-67AD-40FE-86E4-450AF522F174
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemPermission.md
ms.openlocfilehash: 82dac83b9e252e154cedb50f7a3b90a1a78c01c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549023"
---
# <span data-ttu-id="3e010-101">Set-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="3e010-101">Set-AzureRmDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="3e010-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3e010-102">SYNOPSIS</span></span>
<span data-ttu-id="3e010-103">Modyfikuje liczbę ósemkową uprawnień pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3e010-103">Modifies the permission octal of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e010-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3e010-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Permission] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e010-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3e010-105">DESCRIPTION</span></span>
<span data-ttu-id="3e010-106">Polecenie cmdlet **Set-AzureRmDataLakeStoreItemPermission** modyfikuje liczbę ósemkową określoną przez plik lub folder w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3e010-106">The **Set-AzureRmDataLakeStoreItemPermission** cmdlet modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="3e010-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3e010-107">EXAMPLES</span></span>

### <span data-ttu-id="3e010-108">Przykład 1: Ustawianie liczby ósemkowej uprawnień dla elementu</span><span class="sxs-lookup"><span data-stu-id="3e010-108">Example 1: Set the permission octal for an item</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt" -Permission 0770
```

<span data-ttu-id="3e010-109">To polecenie umożliwia ustawienie liczby ósemkowej uprawnień dla pliku na 0770, co tłumaczy, aby wyczyścić bit, ustawić uprawnienia do odczytu/zapisu/wykonywania dla właściciela pliku, ustawić uprawnienia do odczytu/zapisu/wykonywania dla grupy plików, a następnie wyczyścić uprawnienia do odczytu/zapisu/wykonywania.</span><span class="sxs-lookup"><span data-stu-id="3e010-109">This command sets the permission octal for a file to 0770, which translates to clearing the sticky bit, setting read/write/execute permissions for the owner of the file, setting read/write/execute permissions for the owning group of the file, and clearing read/write/execute permissions for other.</span></span>

## <span data-ttu-id="3e010-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3e010-110">PARAMETERS</span></span>

### <span data-ttu-id="3e010-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="3e010-111">-Account</span></span>
<span data-ttu-id="3e010-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3e010-112">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e010-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e010-113">-DefaultProfile</span></span>
<span data-ttu-id="3e010-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3e010-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e010-115">-Path</span><span class="sxs-lookup"><span data-stu-id="3e010-115">-Path</span></span>
<span data-ttu-id="3e010-116">Określa ścieżkę pliku lub folderu w usłudze Data Lake Store, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="3e010-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e010-117">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="3e010-117">-Permission</span></span>
<span data-ttu-id="3e010-118">Uprawnienia do ustawiania pliku lub folderu wyrażone jako ósemkowa (na przykład ' 777 ')</span><span class="sxs-lookup"><span data-stu-id="3e010-118">The permissions to set for the file or folder, expressed as an octal (e.g. '777')</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e010-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3e010-119">-Confirm</span></span>
<span data-ttu-id="3e010-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e010-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e010-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e010-121">-WhatIf</span></span>
<span data-ttu-id="3e010-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e010-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e010-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3e010-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e010-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e010-124">CommonParameters</span></span>
<span data-ttu-id="3e010-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e010-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e010-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e010-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e010-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e010-127">INPUTS</span></span>

### <span data-ttu-id="3e010-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3e010-128">None</span></span>
<span data-ttu-id="3e010-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="3e010-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3e010-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3e010-130">OUTPUTS</span></span>

### <span data-ttu-id="3e010-131">logiczną</span><span class="sxs-lookup"><span data-stu-id="3e010-131">bool</span></span>
<span data-ttu-id="3e010-132">Zwraca wartość Prawda po pomyślnym zaktualizowaniu uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="3e010-132">Returns true upon successfully updating the permission.</span></span>

## <span data-ttu-id="3e010-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3e010-133">NOTES</span></span>
* <span data-ttu-id="3e010-134">Alias: Set-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="3e010-134">Alias: Set-AdlStoreItemPermission</span></span>

## <span data-ttu-id="3e010-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e010-135">RELATED LINKS</span></span>

[<span data-ttu-id="3e010-136">Get-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="3e010-136">Get-AzureRmDataLakeStoreItemPermission</span></span>](./Get-AzureRmDataLakeStoreItemPermission.md)


