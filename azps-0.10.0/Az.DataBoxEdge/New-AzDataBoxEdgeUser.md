---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
ms.openlocfilehash: 480c0a8e932b672542595983f33fd19bab6fec3b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893214"
---
# <span data-ttu-id="7c6a1-101">New-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="7c6a1-101">New-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="7c6a1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7c6a1-102">SYNOPSIS</span></span>
<span data-ttu-id="7c6a1-103">Tworzy nowego użytkownika dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="7c6a1-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="7c6a1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7c6a1-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c6a1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7c6a1-105">DESCRIPTION</span></span>
<span data-ttu-id="7c6a1-106">Polecenie cmdlet **New-AzDataBoxEdgeUser** umożliwia utworzenie nowego użytkownika dla urządzenia z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="7c6a1-106">The **New-AzDataBoxEdgeUser** cmdlet creates a new user for the Data Box Edge device.</span></span> <span data-ttu-id="7c6a1-107">Możliwość tworzenia tylko użytkowników typu `Share` jest obsługiwana.</span><span class="sxs-lookup"><span data-stu-id="7c6a1-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="7c6a1-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7c6a1-108">EXAMPLES</span></span>

### <span data-ttu-id="7c6a1-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7c6a1-109">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

```powershell
PS C:\> New-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key -Type Share
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

## <span data-ttu-id="7c6a1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7c6a1-110">PARAMETERS</span></span>

### <span data-ttu-id="7c6a1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c6a1-111">-AsJob</span></span>
<span data-ttu-id="7c6a1-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7c6a1-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c6a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c6a1-113">-DefaultProfile</span></span>
<span data-ttu-id="7c6a1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7c6a1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c6a1-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="7c6a1-115">-DeviceName</span></span>
<span data-ttu-id="7c6a1-116">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="7c6a1-116">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c6a1-117">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="7c6a1-117">-EncryptionKey</span></span>
<span data-ttu-id="7c6a1-118">Klucz szyfrowania urządzenia brzegowego</span><span class="sxs-lookup"><span data-stu-id="7c6a1-118">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c6a1-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7c6a1-119">-Name</span></span>
<span data-ttu-id="7c6a1-120">Nazwie</span><span class="sxs-lookup"><span data-stu-id="7c6a1-120">Username</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c6a1-121">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="7c6a1-121">-Password</span></span>
<span data-ttu-id="7c6a1-122">Hasło podaj jako bezpieczny ciąg</span><span class="sxs-lookup"><span data-stu-id="7c6a1-122">Password, provide as a secure string</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c6a1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c6a1-123">-ResourceGroupName</span></span>
<span data-ttu-id="7c6a1-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7c6a1-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c6a1-125">-Type</span><span class="sxs-lookup"><span data-stu-id="7c6a1-125">-Type</span></span>
<span data-ttu-id="7c6a1-126">Wybierz pozycję UserType</span><span class="sxs-lookup"><span data-stu-id="7c6a1-126">Select UserType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c6a1-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7c6a1-127">-Confirm</span></span>
<span data-ttu-id="7c6a1-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c6a1-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c6a1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c6a1-129">-WhatIf</span></span>
<span data-ttu-id="7c6a1-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c6a1-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c6a1-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7c6a1-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c6a1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c6a1-132">CommonParameters</span></span>
<span data-ttu-id="7c6a1-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c6a1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c6a1-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c6a1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c6a1-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7c6a1-135">INPUTS</span></span>

### <span data-ttu-id="7c6a1-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7c6a1-136">None</span></span>

## <span data-ttu-id="7c6a1-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7c6a1-137">OUTPUTS</span></span>

### <span data-ttu-id="7c6a1-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="7c6a1-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="7c6a1-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7c6a1-139">NOTES</span></span>

## <span data-ttu-id="7c6a1-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7c6a1-140">RELATED LINKS</span></span>
